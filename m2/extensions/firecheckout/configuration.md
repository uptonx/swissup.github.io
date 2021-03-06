---
layout: default
title: Firecheckout Configuration
description: Firecheckout Configuration
keywords: firecheckout, options, configuration
category: Firecheckout
---

# Configuration

* TOC
{:toc}

### General section

![General section](/images/m2/firecheckout/configuration/general.png)

Option      | Description
------------|------------
Enabled     | Allows to enable/disable firecheckout per store view
Url Path    | Set custom url to the firecheckout page
After Adding a Product Redirect to Firecheckout | Allows to redirect to firecheckout page after Add to Cart action

> If `After Adding a Product Redirect to Firecheckout` is not working on your
> site, try to enable `After Adding a Product Redirect to Shopping Cart` at
> _Stores > Configuration > Checkout > Shopping Cart_ section

### Design section

![Design section](/images/m2/firecheckout/configuration/design.png)

Option      | Description
------------|------------
Page Layout | [Select page layout](#page-layout) to use at firecheckout page
Layout      | [Select layout](#layout) to use at firecheckout page
Theme       | [Select theme](#theme) to use at firecheckout page
Form Styles | [Select form styles](#form-styles) to use at firecheckout page

#### Page Layout

There are 3 page layouts available to use:

 -  [Default Checkout Layout](#&gid=1&pid=1) (Depends on your active theme)
 -  [Empty](#&gid=1&pid=2) (No Header and Footer)
 -  [Minimal](#&gid=1&pid=3) (Header with Store Logo only)
 -  [Full](#&gid=1&pid=4) (Full 1column layout with header, navigation and footer)

Page layout screenshots:

{% include gallery.html images=site.data.gallery.m2.firecheckout.configuration.page-layout class="scroll phone-up-1 tablet-up-4 photoswipe" %}

#### Layout

There are 5 layouts available to use:

 -  [1 Column (Multistep Wizard)](#&gid=2&pid=1)
 -  [1 Column (Expanded)](#&gid=2&pid=2)
 -  [2 Columns (Wide Payment and Shipping sections)](#&gid=2&pid=3)
 -  [2 Columns (Place Payment and Shipping sections side by side)](#&gid=2&pid=4)
 -  [3 Columns](#&gid=2&pid=5)

Layout screenshots:

{% include gallery.html images=site.data.gallery.m2.firecheckout.configuration.layout class="scroll phone-up-1 tablet-up-3 photoswipe" %}

#### Theme

There are 2 themes available to use:

 -  [Default](#&gid=3&pid=1)
 <!-- -  [Dark](#&gid=3&pid=2) -->
 -  [Light](#&gid=3&pid=2)
 -  [Round](#&gid=3&pid=3)

Themes screenshots:

{% include gallery.html images=site.data.gallery.m2.firecheckout.configuration.theme class="scroll phone-up-1 tablet-up-3 photoswipe" %}

#### Form Styles

There are three form **modes** available:

 -  [Horizontal](#&gid=4&pid=1) (Label aside of the field)
 -  [Basic](#&gid=4&pid=2) (Same as horizontal, except label above the field)
 -  [Compact](#&gid=4&pid=3) (Multiple fields per row. [How to change field size?](/m2/extensions/firecheckout/customization/use-cases/field-size/))

{% include gallery.html images=site.data.gallery.m2.firecheckout.configuration.form-styles class="scroll phone-up-1 tablet-up-3 photoswipe" %}

**Use field placeholders instead of labels** - You can hide labels and use field
placeholders instead. This option works together with **Basic** and **Compact**
modes only:

{% include gallery.html images=site.data.gallery.m2.firecheckout.configuration.hidden-labels class="scroll phone-up-1 tablet-up-3 photoswipe" %}

**Show field errors and notices in the Tooltips** - Allows you to switch between
awesome Tooltips mode and Magento's old-school notices and errors below the fields:

{% include gallery.html images=site.data.gallery.m2.firecheckout.configuration.tooltips class="scroll phone-up-1 tablet-up-3 photoswipe" %}

### Additional content section

![Additional content section](/images/m2/firecheckout/configuration/additional-content.png)

Option                  | Description
------------------------|------------
Above Firecheckout Form | Additional content above firecheckout form
Below Firecheckout Form | Additional content below firecheckout form
Above place order button| Additional content above place order button
Below place order button| Additional content below place order button

### Shiping settings section

![Shipping settings section](/images/m2/firecheckout/configuration/shipping.png)

Option                  | Description
------------------------|------------
Default Method          | Default shipping method to use
Default Method Code     | Same setting as above. Use this field if you can't find the method you are looking for in the previous option
Hide methods if single method is available only | Useful if you use single method for all customers

### Payment settings section

![Payment settings section](/images/m2/firecheckout/configuration/payment.png)

Option                  | Description
------------------------|------------
Default Method          | Default payment method to use

### Order summary settings section

![Order summary settings section](/images/m2/firecheckout/configuration/order-summary.png)

Option                  | Description
------------------------|------------
Show Order Review       | Show order review information (Shipping Address and Shiping Method) above the cart items.

### Custom CSS and JS settings section

![Custom CSS and JS settings section](/images/m2/firecheckout/configuration/custom_css_js.png)

Option  | Description
--------|------------
CSS     | CSS styles. LESS is not supported.
JS      | JS code

> **Attention!**
>
> Unlike js code inserted into custom.js file (begins with "define" function),
> code inserted in JS section begins with "require" function.

JS code example:

```js
require([
    'Magento_Ui/js/lib/view/utils/async'
], function($) {
    'use strict';

    var expandables = [
        '.discount-code',
        '.order-attachments'
    ];

    $.async({
        selector: expandables.join(','),
        ctx: $('.checkout-container').get(0)
    }, function (el) {
        setTimeout(function() {
            $(el).collapsible('activate');
        }, 500);
    });
});
```

#### Next up
{:.no_toc}

 -  [Back to Main Page](../)
