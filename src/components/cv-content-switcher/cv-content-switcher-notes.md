# cv-content-switcher

A Vue implementation of a Carbon Components content switcher.

http://www.carbondesignsystem.com/components/content-switcher/code

## Usage

###

```html
<cv-content-switcher @selected="actionSelected">
  <cv-content-switcher-button owner-id="csb-1" :selected="isSelected(0)"
    >Button Name 1</cv-content-switcher-button
  >
  <cv-content-switcher-button owner-id="csb-2" :selected="isSelected(1)"
    >Button Name 2</cv-content-switcher-button
  >
  <cv-content-switcher-button owner-id="csb-3" :selected="isSelected(2)"
    >Button Name 3</cv-content-switcher-button
  >
</cv-content-switcher>

<section style="margin: 10px 0;">
  <cv-content-switcher-content owner-id="csb-1">
    <p>This is the content for option 1</p>
  </cv-content-switcher-content>
  <cv-content-switcher-content owner-id="csb-2">
    <p>This is the content for option 2</p>
  </cv-content-switcher-content>
  <cv-content-switcher-content owner-id="csb-2">
    <p>This is more content for option 2</p>
  </cv-content-switcher-content>
  <cv-content-switcher-content owner-id="csb-3">
    <p>This is the content for option 3</p>
  </cv-content-switcher-content>
</section>
```

### Uses direct DOM manipulation

```html
<cv-content-switcher>
  <cv-content-switcher-button content-selector=".content-1" selected
    >Button Name 1</cv-content-switcher-button
  >
  <cv-content-switcher-button content-selector=".content-2"
    >Button Name 2</cv-content-switcher-button
  >
  <cv-content-switcher-button content-selector=".content-3"
    >Button Name 3</cv-content-switcher-button
  >
</cv-content-switcher>

<section>
  <div class="content-1"><p>This is the content for option 1</p></div>
  <div class="content-2" hidden><p>This is the content for option 2</p></div>
  <div class="content-2" hidden><p>This is more content for option 2</p></div>
  <div class="content-3" hidden><p>This is the content for option 3</p></div>
</section>
```

## Attributes

### CvContentSwitcherButton

- ownerId : Used with CvContentSwitcherPanel
- content-selector : DOM CSS selector used to manipulate the DOM directly. NOTE: Prefer ownerId

NOTE:

- If CvContentSwitcherButtons are added the content they control will react based on the selected property.
- If CvContentSwitcherButtons are removed they content they controll will be displayed.

### CvContentSwitcherPanel

- ownerId : matches one or more values of ownerId in CvContentSwitcherButton

## Events

### CvContentSwitcher

- selected
  - contentSelector
