---
title: KDE Configuration
tags: [personal, guide]
---

Please follow along with this guide in order to set all of the relevant configuration settings which personalize KDE in the way that I like.

For sections which are excluded entirely: just use the platform defaults for all settings.

# Appearance

## Fonts

For hi-DPI screen (like camshaft), use 10-point font for everything except *small*. For other screens (like kinklink), use the same but with 9-point font for *toolbar*.

# Workspace

## Desktop Behavior

### Desktop Effects

Starting from the *Defaults*, disable these effects:
* *Accessibility* -> *Zoom*
* *Appearance* -> *Background contrast*
* *Appearance* -> *Blur*
* *Appearance* -> *Fade*
* *Appearance* -> *Login*
* *Appearance* -> *Maximize*
* *Appearance* -> *Morphing popups*
* *Appearance* -> *Translucency*
* *Appearance* -> *Window Aperture*
* *Appearance* -> *logout*
* *Appearance* -> *Minimize Animation*
* *Virtual Desktop Switching Animation* -> *Slide*
* *Window Management* -> *Desktop Grid*
* *Window Management* -> *Present Windows*

Enable these effects:
* *Appearance* -> *Desaturate Unresponsive Applications* (>= KDE 5.10)
* *Appearance* -> *Screen Edge*
* *Appearance* -> *Sliding popups*
* *Focus* -> *Dialog Parent*
* *Focus* -> *Dim Screen for Administrator Mode*

### Screen Edges

Add the *Application Launcher* action to the lower-left corner of the screen. Clear all other corner/edge actions.

### Screen Locking

Change from 5 min to 10 min.

### Virtual Desktops

#### Desktops

Set number of desktops to 3, and number of rows to 3. Use the names *Alpha*, *Beta*, and *Gamma*. Ignore the message "could not set shortcut Ctrl+F3 for Desktop 3" if it appears.

#### Switching

Disable *Desktop navigation wraps around*. Disable the keyboard shortcuts for switching directly to desktops, and enable *Ctrl+Alt+Up* and *Ctrl+Alt+Down* for switching up and down, respectively.

### Accessibility (<= KDE 5.8)

### Bell

Disable *Use system bell*.

### Activities

#### Activities

Rename *Default* to *Personal*, and create a *Work* activity. Use a house icon for *Personal* and a mail icon for *Work*.

#### Switching

Disable the keyboard shortcuts for *Walk through activities* and *Walk through actvities (Reverse)*.

## Window Management

### Window Behavior

#### Focus

Change *Activating windows* policy to *Focus Follows Mouse - Mouse Precedence*. Reduce the focus delay to 50 ms. Change *Focus stealing prevention* to *None*.

#### Titlebar Actions

Clear all of the other actions besides these four:

* *Titlebar* -> *Double-click* (keep as *Maximize*)
* *Titlebar & Frame* -> *Active and Inactive Left button* (keep as *Raise* and *Activate & Raise*, respectively)
* *Titlebar & Frame* -> *Active and Inactive Right button* (keep both as *Operations Menu*)
* *Maximize Button* -> *Left button* (keep as *Maximize*) and set the others to the same

#### Window Actions

Keep all *Inactive Inner Window* settings the same. Clear all *Inner Window, Titlebar & Frame* except *Left button*, and change *Modifier key* to *Meta*.

### Task Switcher (Main)

For *All windows*, change *Forward* shortcut to *Meta+Tab* and change *Reverse* shortcut to *Meta+Shift+Tab*. Similarly, switch *Alt* to *Meta* for the *Current application* switcher.

Enable *Include "Show Desktop" icon* and *Only one window per application*.

## Shortcuts

### Standard Shortcuts

Change *Full Screen Mode* to *F11*.

### Global Shortcuts

#### Accessibility (>= KDE 5.10) or kaccess (<= KDE 5.8)

Disable *Toggle Screen Reader On and Off*.

#### Plasma (>= KDE 5.10) or Activity switching (<= KDE 5.8)

Change *Activate Application Launcher Widget* to *Meta+Space*. Disable *Activities...*

#### Power Management

Change *Show System Activity* to *Ctrl+Alt+Del*. This may override the *Log Out* action, which we will be clearing anyway, so confirm the reassignment.

#### Run Command

Clear all keyboard combinations within this page.

#### System Settings

Change all of these settings:
* *Activate Window Demanding Attention*: *Ctrl+Alt+A* -> *none*
* *Actual Size*: *Meta+0* -> *none*
* *Halt Without Confirmation*: *Ctrl+Alt+Shift+PgDown* -> *none*
* *Kill Window*: *Ctrl+Alt+Esc* -> *none*
* *Lock Session (alternate)*: *none* -> *Meta+L*
* *Log Out Without Confirmation*: *Ctrl+Alt+Shift+Del* -> *none*
* *Maximize Window*: *none* -> *Meta+Up*
* *Move Mouse to Center*: *Meta+F6* -> *none*
* *Move Mouse to Focus*: *Meta+F5* -> *none*
* *Move Zoomed Area Downwards*: *Meta+Down* -> *none*
* *Move Zoomed Area to Left*: *Meta+Left* -> *none*
* *Move Zoomed Area to Right*: *Meta+Right* -> *none*
* *Move Zoomed Area Upwards*: *Meta+Up* -> *none*
* *Quick Tile Window to the Left*: *none* -> *Meta+Left*
* *Quick Tile Window to the Right*: *none* -> *Meta+Right*
* *Reboot Without Confirmation*: *Ctrl+Alt+Shift+PgUp* -> *none*
* *Show Desktop Grid*: *Ctrl+F8* -> *none*
* *Suspend Compositing*: *Alt+Shift+F12* -> *none*
* *Switch to Desktop N*: *Ctrl+FN* -> *none* (all of them)
* *Switch to Window Above*: *Meta+Alt+Up* -> *none*
* *Switch to Window Below*: *Meta+Alt+Below* -> *none*
* *Switch to Window to the Left*: *Meta+Alt+Left* -> *none*
* *Switch to Window to the Right*: *Meta+Alt+Right* -> *none*
* *Toggle Present Windows (All desktops)*: *Ctrl+F10* -> *none*
* *Toggle Present Windows (All desktops) alternate*: *Launch (C)* -> *none*
* *Toggle Present Windows (Current desktop)*: *Ctrl+F9* -> *none*
* *Toggle Present Windows (Window class)*: *Ctrl+F7* -> *none*
* *Window One Desktop Down*: *none* -> *Ctrl+Alt+Shift+Down*
* *Window One Desktop Up*: *none* -> *Ctrl+Alt+Shift+Up*
* *Window Operations Menu*: *Alt+F3* -> *none*
* *Zoom In*: *Meta+=* -> *none*
* *Zoom Out*: *Meta+-* -> *none*

### Web Shortcuts

Disable Web shortcuts.

### Custom Shortcuts

Create a new *Global Shortcut* -> *Command / URL* called *Terminal* with trigger *Meta+Return* and action *konsole*.

## Startup and Shutdown

### Desktop Session

On login, choose the *Start with an empty session* option.

## Search

### Plasma Search

Disable the *Web Shortcuts* plugin.

# Personalization

## Notifications

### Event source: Local system message service (<= KDE 5.8)

Disable sounds for all of these events.

### Event source: Notifies when a new printer is detected (>= KDE 5.10)

Disable sounds for all of these events.

### Event source: On-Screen Ruler

Disable sounds for all of these events.

### Event source: Plasma Workspace

First, disable sounds for all of these events. Then, set *Oxygen-Sys-App-Message.ogg* for all of the following:

* *Warning*
* *Question*
* *Warning Message*
* *Critical Message*
* *Catastrophe*
* *Fatal Error*

### Event source: Power Management System

As before, disable sounds for all of these events. Then, set *Oxygen-Sys-App-Message.ogg* for *Battery Low* and *Battery Critical*.

### Event source: Touchpad

Disable sounds for all of these events.

## Applications

### Default Applications

Change *Web Browser* to explicitly open *http and https URLs* using a command: */home/louis/bin/firefox_activity_wrapper.sh*.

### File Associations

For all of these: if the MIME type does not already exist, *there is no need to create it*. Only change the setting if it already exists.

Move *Visual Studio Code* to the top spot for all of these MIME types:
* *application/javascript*
* *application/xhtml+xml*
* *application/xml*
* *application/xml-dtd*
* *application/xml-external-parsed-entity*
* *text/css*
* *text/markdown*
* *text/plain*
* *text/x-fortran*
* *text/x-makefile*
* *text/x-python*
* *text/x-python3*

Move *VLC* to the top spot for all of these MIME types:
* *application/ogg*
* *application/x-matroska*
* Everything underneath *audio*
* Everything under *video*

Ensure that *application/pdf* is opened in *Document Viewer* (a.k.a. *Okular*). Ensure that *application/rtf* is opened in *LibreOffice Writer*. Ensure that *text/html* is opened in *Firefox Latest* (on Debian) or plain *Firefox* (on Fedora).

For every *image/\** entry where more than one image program is available, move *GIMP* **below** the top spot. It is not a good image previewer. However, leave it as the top choice for *image/x-compressed-xcf* and *image/x-xcf*.

## Accessibility

### Bell

Disable *Use system bell*.

# Network

## Connections (>= KDE 5.10)

Connect to wireless networks, set IP settings, etc.

## Settings

### Proxy

Configure proxy to use an auto configuration URL: [http://localhost:8081/www-proxy.pac](http://localhost:8081/www-proxy.pac)

# Hardware

## Input Devices

### Keyboard

#### Layouts

Clear the three shortcuts (*Main*, *3rd level*, and *Alternative*) for switching layout.

#### Advanced

Check the box to *Configure keyboard options*. Clear all of the remaining boxes except *Position of Compose key*. Underneath that option, select the check box next to *Menu*.

### Mouse

Under *Icons*, select *Double-click to open files and folders (select icons on first click)*.

## Display and Monitor

### Displays

Arrange and order displays as desired.

## Power Management (for laptop only)

### Energy Saving

Underneath all three settings  (*On AC Power*, *On Battery*, and *On Low Battery*), switch event *when laptop lid closed* to *Suspend*. Also, enable *Screen brightness* control and set the slider to max for AC or a reasonable level for battery.

### Advanced Settings

At critical battery, choose to *Suspend* rather than to *Hibernate*. Increase *Low level* to 15% and *Critical level* to 10%.

# Miscellaneous (not actually in System Settings)

## Firefox profiles

Ensure that there is one Firefox profile for each of the different Activities. Replace the *Command* for the default Firefox browser with an invocation of */home/louis/bin/firefox_activity_wrapper.sh*.

## Desktop Settings (Plasma)

Right-click anywhere in the empty space for this menu.

### Mouse Actions

Disable the *Vertical Scroll* action (which was *Switch Desktop*).
