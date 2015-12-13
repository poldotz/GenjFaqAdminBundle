# GenjFaqAdminBundle

The GenjFaqAdminBundle enables the admin for GenjFaqBundle.


## Installation

Add this to your composer.json:

```
    ...
    "repositories": [
        {
            "type": "vcs",
            "url": "git.genj.nl:bundles/GenjAdminBundle.git"
        },
        {
            "type": "vcs",
            "url": "git.genj.nl:bundles/GenjFaqAdminBundle.git"
        },
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
