---
layout: default
title: Navigationpro Nowrap Feature
description: >
    How to move top-level items into separate dropdown, when there is not
    enough space to fit menu in a single line
category: Navigationpro
---

# Nowrap (Single row menu)

Nowrap - is a feature that allows to move top-level items into separate dropdown,
when there is not enough space to fit on a single row.

![Nowrap](/images/m2/navigationpro/use-cases/nowrap.png)

Nowrap feature automatically hides last menu items to guarantee that menu will
fit on a single row.

To activate nowrap feature, you need to add `navpro-nowrap` class to the
[CSS Class field](/m2/extensions/navigationpro/backend/menu-settings/#general-settings).

> **Warning!**
>
> Nowrap works well with the following conditions only:
>  - Menu is on the separate row
>  - Menu takes all amout of available width of parent container
>
> Otherwise it may be tricky to
> make it work properly (Custom work and advanced CSS knowledge may be required).

#### Next up

 -  [Back to Main Page](/m2/extensions/navigationpro/)
 -  [CSS Helpers][css-helpers]

[css-helpers]: /m2/extensions/navigationpro/customization/css-helpers/ "CSS Helpers"
