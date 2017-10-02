[![Build Status](https://travis-ci.org/zeroincombenze/stock-logistics-barcode.svg?branch=10.0)](https://travis-ci.org/zeroincombenze/stock-logistics-barcode)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/stock-logistics-barcode/badge.svg?branch=10.0)](https://coveralls.io/github/zeroincombenze/stock-logistics-barcode?branch=10.0)
[![codecov](https://codecov.io/gh/zeroincombenze/stock-logistics-barcode/branch/10.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/stock-logistics-barcode/branch/10.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-10.svg)](https://github.com/OCA/stock-logistics-barcode/tree/10.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/man/LO)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-10.svg)](http://erp10.zeroincombenze.it)


[![en](https://github.com/zeroincombenze/grymb/blob/master/flags/en_US.png)](https://www.facebook.com/groups/openerp.italia/)
================================================================================================
================================================================================================

Odoo Stock Logistic Barcode
===========================


This project aims to deal with modules related to the management of barcode in a generic way. You'll find modules that:

 - Allow to generate bar code each time a object is created
 - Setup bar code on object
 - Print bar code
 - Search and use them with a barcode scanner

Please don't hesitate to suggest one of your module to this project. Also, you may want to have a look on those other projects here:

 - https://github.com/OCA/stock-logistics-tracking
 - https://github.com/OCA/stock-logistics-workflow
 - https://github.com/OCA/stock-logistics-warehouse

[//]: # (addons)


Available addons
----------------
addon | version | OCA version | summary
--- | --- | --- | ---
[barcodes_generator_abstract](barcodes_generator_abstract/) | 10.0.1.0.0 | 10.0.1.0.1 | Generate Barcodes for Any Models
[barcodes_generator_location](barcodes_generator_location/) | 10.0.1.0.0 | :repeat: | Generate Barcodes for Stock Locations
[barcodes_generator_lot](barcodes_generator_lot/) | 10.0.1.0.0 | :repeat: | Generate Barcodes for Stock Production Lots
[barcodes_generator_package](barcodes_generator_package/) | 10.0.1.0.0 | :repeat: | Generate Barcodes for Product Packaging
[barcodes_generator_partner](barcodes_generator_partner/) | 10.0.1.0.0 | :repeat: | Generate Barcodes for Partners
[barcodes_generator_product](barcodes_generator_product/) | 10.0.1.0.0 | :repeat: | Generate Barcodes for Products (Templates and Variants)
[stock_scanner](stock_scanner/) | 10.0.1.0.0 | :repeat: | Allows managing barcode readers with simple scenarios


Unported addons
---------------
addon | version | OCA version | summary
--- | --- | --- | ---
[barcode_link](barcode_link/) | 1.0 (unported) | :repeat: | Barcode link Module
[base_gs1_barcode](base_gs1_barcode/) | 1.0 (unported) | :repeat: | Decoding API for GS1-128 (aka UCC/EAN-128) and GS1-Datamatrix
[product_multi_ean](product_multi_ean/) | 1.2 (unported) | :repeat: | Multiple EAN13 on products

[//]: # (end addons)

[//]: # (copyright)

----

**Odoo** is a trademark of [Odoo S.A.](https://www.odoo.com/) (formerly OpenERP, formerly TinyERP)

**OCA**, or the [Odoo Community Association](http://odoo-community.org/), is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

**zeroincombenze®** is a trademark of [SHS-AV s.r.l.](http://www.shs-av.com/)
which distributes and promotes **Odoo** ready-to-use on its own cloud infrastructure.
[Zeroincombenze® distribution](http://wiki.zeroincombenze.org/en/Odoo)
is mainly designed for Italian law and markeplace.
Everytime, every Odoo DB and customized code can be deployed on local server too.

[//]: # (end copyright)

[![chat with us](https://www.shs-av.com/wp-content/chat_with_us.gif)](https://tawk.to/85d4f6e06e68dd4e358797643fe5ee67540e408b)
