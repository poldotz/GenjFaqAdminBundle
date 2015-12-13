# GenjFaqAdminBundle

The GenjFaqAdminBundle enables the admin for GenjFaqBundle within SonataAdmin.
No SonataAdmin, no FaqAdmin:
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

Then run `composer update`. After that is done, enable the bundle in your AppKernel.php:

```
$bundles[] = new Genj\FaqAdminBundle\GenjFaqAdminBundle();
```
