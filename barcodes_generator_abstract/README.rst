[![Build Status](https://travis-ci.org/zeroincombenze/stock-logistics-barcode.svg?branch=10.0)](https://travis-ci.org/zeroincombenze/stock-logistics-barcode)
[![license lgpl](https://img.shields.io/badge/licence-LGPL--3-7379c3.svg)](https://www.gnu.org/licenses/lgpl.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/stock-logistics-barcode/badge.svg?branch=10.0)](https://coveralls.io/github/zeroincombenze/stock-logistics-barcode?branch=10.0)
[![codecov](https://codecov.io/gh/zeroincombenze/stock-logistics-barcode/branch/10.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/stock-logistics-barcode/branch/10.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-10.svg)](https://github.com/OCA/stock-logistics-barcode/tree/10.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/man/LO)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-10.svg)](http://erp10.zeroincombenze.it)




[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

   :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
   :alt: License: AGPL-3

Generate Barcodes for any Models (Abstract)
===========================================

This module expends Odoo functionality, allowing user to generate barcode
depending on a given barcode rule for any Model.

For example, a typical pattern for products is  "20.....{NNNDD}" that means
that:
* the EAN13 code will begin by '20'
* followed by 5 digits (named Barcode Base in this module)
* and after 5 others digits to define the variable price
* a 13 digit control

With this module, it is possible to:

* Affect a pattern (barcode.rule) to a model

* Define a Barcode base: 
    * manually, if the base of the barcode must be set by a user. (typically an
      internal code defined in your company)
    * automaticaly by a sequence, if you want to let Odoo to increment a
      sequence. (typical case of a customer number incrementation)

* Generate a barcode, based on the defined pattern and the barcode base

Installation
------------






This module use an extra python library named 'viivakoodi' you should install
to make barcode generation works properly. 'viivakoodi' is a more active for of
'pyBarcode'.

``sudo pip install viivakoodi``

Configuration
-------------






To configure this module, you need to:

* Go to Settings / Technical / Sequences & Identifiers / Barcode Nomenclatures
* Select a Nomenclature
* Create or select a rule

.. image:: /barcodes_generator_abstract/static/description/barcode_rule_tree.png

* For manual generation, set:
    * 'Base set Manually' in 'Generate Type'
    * Set the model

.. image:: /barcodes_generator_abstract/static/description/barcode_rule_form_manual.png

* For automatic generation, set:
    * 'Base managed by Sequence' in 'Generate Type'
    * Set the model
    * Generate a new sequence by button, or affect a existing one

.. image:: /barcodes_generator_abstract/static/description/barcode_rule_form_sequence.png

In all cases, padding will be computed automaticaly, based on the number
of '.' in the Barcode Pattern field.

Usage
-----






=====

This module is an abstract module. You can configure Barcode Rule, but to
enable this feature, you need to install an extra module for a given model.
This repository provide 'barcodes_generator_product' and
'barcodes_generator_partner' module to generate barcode for product or partner
model.

Alternatively, you can develop a custom module for a custom model. See
'Inheritance' parts.

Try this module on Runbot

.. image:: https://odoo-community.org/website/image/ir.attachment/5784_f2813bd/datas
   :alt: Try me on Runbot
   :target: https://runbot.odoo-community.org/runbot/150/10.0

Inheritance

If you want to generate barcode for another model, you can create a custom
module that inherits on 'barcodes_generator_abstract' and inherit your model
like that:

class MyModel(models.Model):
    _name = 'my.model'
    _inherit = ['my.model', 'barcode.generate.mixin']

class barcode_rule(models.Model):
    _inherit = 'barcode.rule'

    generate_model = fields.Selection(selection_add=[('my.model', 'My Model')])

Finally, you should inherit your model view adding buttons and fields.

Note
----

Your model should have a field 'barcode' defined.

Known issues / Roadmap
----------------------






1. On barcode.rule model, constraint and domain system could be set between
   'type' and 'generate_model' fields.
1. Cache is being cleared in a constraint in `barcode.rule`. Mutating in a
   constraint is bad practice & should be moved somewhere.

Bug Tracker
-----------






Bugs are tracked on `GitHub Issues
<https://github.com/OCA/stock-logistics-barcode/issues>`_. In case of trouble,
please check there if your issue has already been reported. If you spotted it
first, help us smashing it by providing a detailed and welcomed feedback.

Credits
-------






Images

* Icon of the module is based on the Oxygen Team work and is under LGPL licence:
  http://www.iconarchive.com/show/oxygen-icons-by-oxygen-icons.org.html






### Contributors






* Sylvain LE GAL (https://twitter.com/legalsylvain)
* Dave Lasley <dave@laslabs.com>

### Funders

### Maintainer










.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

This module is maintained by the OCA.

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

To contribute to this module, please visit https://odoo-community.org.

[//]: # (copyright)

----

**Odoo** is a trademark of [Odoo S.A.](https://www.odoo.com/) (formerly OpenERP, formerly TinyERP)

**OCA**, or the [Odoo Community Association](http://odoo-community.org/), is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

**zeroincombenze®** is a trademark of [SHS-AV s.r.l.](http://www.shs-av.com/)
which distributes and promotes **Odoo** ready-to-use on own cloud infrastructure.
[Zeroincombenze® distribution of Odoo](http://wiki.zeroincombenze.org/en/Odoo)
is mainly designed for Italian law and markeplace.
Users can download from [Zeroincombenze® distribution](https://github.com/zeroincombenze/OCB) and deploy on local server.

[//]: # (end copyright)

[//]: # (addons)

[//]: # (end addons)



[![chat with us](https://www.shs-av.com/wp-content/chat_with_us.gif)](https://tawk.to/85d4f6e06e68dd4e358797643fe5ee67540e408b)
