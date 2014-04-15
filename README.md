# o-aside

___
Titled content module with optional multiple panels.
___

Status: Gathering requirements...

## Example use case

![FT.com rail module](https://github.com/Financial-Times/o-aside/raw/master/files/rail-module.png "FT.com rail module")

This module will provide styling for:

* Title
* Tabs (optional)
* Tabpanels (minimum of 1)

It will not provide the styling for the contents of the tabpanels.

[o-tabs](https://github.com/Financial-Times/o-tabs) will be used for the tabs' behaviour.

This module will ensure that any content below the __o-aside__ will not shift up and down due to variations of the __o-aside__ tabpanels' heights.


## Draft markup

__Without tabs___

```html
<aside data-o-component="o-aside" data-o-version="1.0.0" class="o-aside">
    <h3 class="o-aside__title">Title</h3>
    <div class="o-aside__tabpanel o-tabs__tabpanel">
        o-aside content
    </div>
</aside>
```

__With tabs__

```html
<aside data-o-component="o-aside" data-o-version="1.0.0" class="o-aside">
    <h3 class="o-aside__title">Title</h3>
    <ul data-o-component="o-tabs" data-o-version="1.0.0" class="o-tabs" role="tablist">
        <li role="tab"><a href="#oAsideContent1">Tab 1</a></li>
        <li role="tab"><a href="#oAsideContent2">Tab 2</a></li>
        <li role="tab"><a href="#oAsideContent3">Tab 3</a></li>
    </ul>
    <div id="oAsideContent1" class="o-aside__tabpanel o-tabs__tabpanel" role="tabpanel">
        o-aside content 1
    </div>
    <div id="oAsideContent2" class="o-aside__tabpanel o-tabs__tabpanel" role="tabpanel">
        o-aside content 2
    </div>
    <div id="oAsideContent3" class="o-aside__tabpanel o-tabs__tabpanel" role="tabpanel">
        o-aside content 3
    </div>
</aside>
```