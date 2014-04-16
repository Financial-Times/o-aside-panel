# o-panel

___
Content module with a heading and one or more panels.
___

Status: Gathering requirements...

## Example use case

![FT.com rail module](https://github.com/Financial-Times/o-panel/raw/master/files/rail-module.png "FT.com rail module")

This module will provide styling for:

* Heading
* Tabs (optional)
* Tabpanels (minimum of 1)

It will not provide the styling for the contents of the tabpanels.

[o-tabs](https://github.com/Financial-Times/o-tabs) will be used for the tabs' behaviour.

This module will ensure that any content below the __o-panel__ will not shift up and down due to variations of the __o-panel__ tabpanels' heights.


## Draft markup

__Without tabs__

```html
<div data-o-component="o-panel" data-o-version="1.0.0" class="o-panel">
    <h3 class="o-panel__heading">Title</h3>
    <div class="o-panel__body">
        o-panel body content
    </div>
</div>
```

__With tabs__

```html
<div data-o-component="o-panel" data-o-version="1.0.0" class="o-panel">
    <h3 class="o-panel__heading">Title</h3>
    <ul data-o-component="o-tabs" data-o-version="1.0.0" class="o-tabs" role="tablist">
        <li role="tab"><a href="#oPanelContent1">Tab 1</a></li>
        <li role="tab"><a href="#oPanelContent2">Tab 2</a></li>
        <li role="tab"><a href="#oPanelContent3">Tab 3</a></li>
    </ul>
    <div id="oPanelContent1" class="o-panel__body o-tabs__tabpanel" role="tabpanel">
        o-panel body content 1
    </div>
    <div id="oPanelContent2" class="o-panel__body o-tabs__tabpanel" role="tabpanel">
        o-panel body content 2
    </div>
    <div id="oPanelContent3" class="o-panel__body o-tabs__tabpanel" role="tabpanel">
        o-panel body content 3
    </div>
</div>
```