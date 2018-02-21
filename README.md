[![Build Status](https://travis-ci.org/zeroincombenze/stock-logistics-barcode.svg?branch=8.0)](https://travis-ci.org/zeroincombenze/stock-logistics-barcode)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/stock-logistics-barcode/badge.svg?branch=8.0)](https://coveralls.io/github/zeroincombenze/stock-logistics-barcode?branch=8.0)
[![codecov](https://codecov.io/gh/zeroincombenze/stock-logistics-barcode/branch/8.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/stock-logistics-barcode/branch/8.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-8.svg)](https://github.com/OCA/stock-logistics-barcode/tree/8.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-8.svg)](http://wiki.zeroincombenze.org/en/Odoo/8.0/man/LO)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-8.svg)](http://erp8.zeroincombenze.it)
































[![en](http://www.shs-av.com/wp-content/en_US.png)](http://wiki.zeroincombenze.org/it/Odoo/7.0/man)

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
[base_gs1_barcode](base_gs1_barcode/) | 8.0.1.1.0 | :repeat: | Decoding API for GS1-128 (aka UCC/EAN-128) and GS1-Datamatrix
[product_barcode_generator](product_barcode_generator/) | 8.0.1.0.0 | :repeat: | Product barcode generator
[product_multi_ean](product_multi_ean/) | 8.0.1.0.0 | :repeat: | Multiple EAN13 on products
[stock_disable_barcode_interface](stock_disable_barcode_interface/) | 8.0.1.0.0 | :repeat: | Disable and enable (configurable) the barcode interface
[stock_inventory_barcode](stock_inventory_barcode/) | 8.0.0.1.0 | :repeat: | Add simple barcode interface on inventories


Unported addons
---------------
addon | version | OCA version | summary
--- | --- | --- | ---
[barcode_link](barcode_link/) | 1.0 (unported) | :repeat: | Barcode link Module
[tr_barcode](tr_barcode/) | 1.1.4 (unported) | :repeat: | TR Barcode
[tr_barcode_config](tr_barcode_config/) | 1.1.1 (unported) | :repeat: | Barcode configuration Module
[tr_barcode_field](tr_barcode_field/) | 1.1 (unported) | :repeat: | Barcode field Module
[tr_barcode_on_picking](tr_barcode_on_picking/) | 1.1 (unported) | :repeat: | Barcode for pickings
[tr_barcode_on_prodlots](tr_barcode_on_prodlots/) | 1.1 (unported) | :repeat: | Barcode for production lots
[tr_barcode_on_product](tr_barcode_on_product/) | 1.1 (unported) | :repeat: | Barcode for product
[tr_barcode_on_tracking](tr_barcode_on_tracking/) | 1.1 (unported) | :repeat: | Barcode for tracking

[//]: # (end addons)


Translation Status
[![Transifex Status](https://www.transifex.com/projects/p/OCA-stock-logistics-barcode-8-0/chart/image_png)](https://www.transifex.com/projects/p/OCA-stock-logistics-barcode-8-0)

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
