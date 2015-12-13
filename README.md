# GenjFaqAdminBundle

The GenjFaqAdminBundle is an addition to GenjFaqBundle and contains only admin classes for SonataAdmin.
So: no SonataAdmin, no FaqAdmin:
https://sonata-project.org/bundles/admin/2-3/doc/index.html


## Installation

Add this to your composer.json:

```
    ...
        
    "require": {
        ...
        "genj/faq-admin-bundle": "dev-master"
        ...
```

Then run `composer update`. 


After that is done, enable the bundle in your AppKernel.php:

```
$bundles[] = new Genj\FaqAdminBundle\GenjFaqAdminBundle();
```

and in your config.yml for the sonata admin dashboard
```
sonata_admin:
    dashboard:
        groups:
            Content:
                items:
                    - sonata.admin.genj_faq_question
```

By default the FAQ is part of the content group.
If you don't like that, overwrite the service:
```
services:
    sonata.admin.genj_faq_question:
        class: %genj_faq.admin.question_admin.class%
        tags:
            - { name: sonata.admin, manager_type: orm, group: "Content", label: "FAQ" }
```
