---
title: "Class: TouchBarButton"
description: "Create a button in the touch bar for native macOS applications"
slug: touch-bar-button
hide_title: false
---

## Class: TouchBarButton

> Create a button in the touch bar for native macOS applications

Process: [Main](latest/glossary.md#main-process)<br />
_This class is not exported from the `'electron'` module. It is only available as a return value of other methods in the Electron API._

### `new TouchBarButton(options)`

* `options` Object
  * `label` String (optional) - Button text.
  * `accessibilityLabel` String (optional) - A short description of the button for use by screenreaders like VoiceOver.
  * `backgroundColor` String (optional) - Button background color in hex format,
    i.e `#ABCDEF`.
  * `icon` [NativeImage](latest/api/native-image.md) | String (optional) - Button icon.
  * `iconPosition` String (optional) - Can be `left`, `right` or `overlay`. Defaults to `overlay`.
  * `click` Function (optional) - Function to call when the button is clicked.
  * `enabled` Boolean (optional) - Whether the button is in an enabled state.  Default is `true`.

When defining `accessibilityLabel`, ensure you have considered macOS [best practices](https://developer.apple.com/documentation/appkit/nsaccessibilitybutton/1524910-accessibilitylabel?language=objc).

### Instance Properties

The following properties are available on instances of `TouchBarButton`:

#### `touchBarButton.accessibilityLabel`

A `String` representing the description of the button to be read by a screen reader. Will only be read by screen readers if no label is set.

#### `touchBarButton.label`

A `String` representing the button's current text. Changing this value immediately updates the button
in the touch bar.

#### `touchBarButton.backgroundColor`

A `String` hex code representing the button's current background color. Changing this value immediately updates
the button in the touch bar.

#### `touchBarButton.icon`

A `NativeImage` representing the button's current icon. Changing this value immediately updates the button
in the touch bar.

#### `touchBarButton.iconPosition`

A `String` - Can be `left`, `right` or `overlay`.  Defaults to `overlay`.

#### `touchBarButton.enabled`

A `Boolean` representing whether the button is in an enabled state.
