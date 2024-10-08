---
title: Toolbar title rollover delay | Finder
description: Choose the delay of the auto-hidden document-proxy icon.
head:
  - - meta
    - property: 'og:title'
      content: macOS defaults > Finder > Toolbar title rollover delay
  - - meta
    - property: 'og:description'
      content: Choose the delay of the auto-hidden document-proxy icon.
---

# Toolbar title rollover delay

Choose the delay of the auto-hidden document-proxy icon.

- **Tested on macOS**:
  - Ventura
  - Monterey
  - Big Sur
- **Parameter type**: float

## Requirements

- [`com.apple.universalaccess showWindowTitlebarIcons`](/finder/showwindowtitlebaricons.md#set-to-false-default-value) must be set to `false`

## Set to `0.5` (default value)

By default, the toolbar title hovering delay takes 0.5 seconds

```bash
defaults write NSGlobalDomain "NSToolbarTitleViewRolloverDelay" -float "0.5" && killall Finder
```

<video autoplay loop muted playsinline width="741" height="416" style="max-width: 100%; height: auto">
  <source src="./images/NSToolbarTitleViewRolloverDelay/0.5.mp4" type="video/mp4">
  Example output with value set to 0.5
</video>

## Set to `0`

Remove the delay when hovering the toolbar title

```bash
defaults write NSGlobalDomain "NSToolbarTitleViewRolloverDelay" -float "0" && killall Finder
```

<video autoplay loop muted playsinline width="741" height="416" style="max-width: 100%; height: auto">
  <source src="./images/NSToolbarTitleViewRolloverDelay/0.mp4" type="video/mp4">
  Example output with value set to 0
</video>

## Set to `1`

Increase the delay when hovering the toolbar title

```bash
defaults write NSGlobalDomain "NSToolbarTitleViewRolloverDelay" -float "1" && killall Finder
```

<video autoplay loop muted playsinline width="741" height="416" style="max-width: 100%; height: auto">
  <source src="./images/NSToolbarTitleViewRolloverDelay/1.mp4" type="video/mp4">
  Example output with value set to 1
</video>

## Read current value

```bash
defaults read NSGlobalDomain "NSToolbarTitleViewRolloverDelay"
```

## Reset to default value

```bash
defaults delete NSGlobalDomain "NSToolbarTitleViewRolloverDelay" && killall Finder
```
