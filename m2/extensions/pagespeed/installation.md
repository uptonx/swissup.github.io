---
layout: default
title: Pagespeed installation
description: Pagespeed installation instructions
keywords: "Pagespeed installation"
category: Pagespeed
---

# Installation instructions

{% include installation/m2/index.html %}

Run the following commands:

```bash
cd <magento_root>
composer require swissup/pagespeed
php bin/magento module:enable Swissup_Pagespeed
php bin/magento setup:upgrade
php bin/magento setup:di:compile
```

##### Next up

Great! Now you might want to see next:

- [Quick Start](/m2/extensions/pagespeed/quickstart/)
- [Configuration](/m2/extensions/pagespeed/configuration/)
- [Changelog](/m2/extensions/pagespeed/changelog/)
