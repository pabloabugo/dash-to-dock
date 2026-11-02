# Dash to Dock

> [!NOTE]
> **About this fork.** This is a personal fork of [ubuntu/dash-to-dock](https://github.com/ubuntu/dash-to-dock).
> The `pablo` branch is the latest upstream release published on extensions.gnome.org plus:
>
> - **Show pinned applications only on the primary monitor.** New option under
>   *Launchers → Show pinned applications → Only on the primary monitor*
>   (`show-favorites-only-on-primary`). With it, docks on other monitors list only running
>   applications; combine it with *Isolate monitors* to show only the windows on each monitor.
>   Proposed upstream in [ubuntu/dash-to-dock#2774](https://github.com/ubuntu/dash-to-dock/pull/2774)
>   (requested in [#2487](https://github.com/ubuntu/dash-to-dock/issues/2487) and
>   [#555](https://github.com/ubuntu/dash-to-dock/issues/555)).
> - **Website links fixed** (the old micheleg.github.io address returns 404).
>   Proposed upstream in [ubuntu/dash-to-dock#2773](https://github.com/ubuntu/dash-to-dock/pull/2773).
> - **Own UUID `dash-to-dock@pablo`**, so automatic updates from extensions.gnome.org do not
>   replace it. It uses the same settings schema, so install it *instead of* the original
>   extension, not alongside it.
>
> Once the changes are merged upstream, they are dropped from this branch.
> Branches meant for the pull requests contain only the corresponding commits on top of upstream.

![screenshot](https://github.com/micheleg/dash-to-dock/raw/master/media/screenshot.jpg)

## A dock for the GNOME Shell
This extension enhances the dash moving it out of the overview and transforming it in a dock for an easier launching of applications and a faster switching between windows and desktops without having to leave the desktop view.

[<img src="https://ubuntu.github.io/dash-to-dock/media/get-it-on-ego.png" height="100">](https://extensions.gnome.org/extension/307/dash-to-dock)

For additional installation instructions and more information visit [https://ubuntu.github.io/dash-to-dock/](https://ubuntu.github.io/dash-to-dock/).

## Installation from source

The extension can be installed directly from source, either for the convenience of using git or to test the latest development version. Clone the desired branch with git

### Build Dependencies

To compile the stylesheet you'll need an implementation of SASS. Dash to Dock supports `dart-sass` (`sass`), `sassc`, and `ruby-sass`. Every distro should have at least one of these implementations, we recommend using `dart-sass` (`sass`) or `sassc` over `ruby-sass` as `ruby-sass` is deprecated.

By default, Dash to Dock will attempt to build with `sassc`. To change this behavior set the `SASS` environment variable to either `dart` or `ruby`.

```bash
export SASS=dart
# or...
export SASS=ruby
```

### Building

Clone the repository or download the branch from github. A simple Makefile is included.

Next use `make` to install the extension into your home directory. A Shell reload is required <kbd>Alt</kbd> + <kbd>F2</kbd> <kbd>r</kbd> <kbd>Enter</kbd> under Xorg or under Wayland you may have to logout and login. The extension has to be enabled  with *gnome-extensions-app* (GNOME Extensions) or with *dconf*.

```bash
git clone https://github.com/micheleg/dash-to-dock.git
make -C dash-to-dock install
```

If `msgfmt` is not available on your system, you will see an error message like the following:

```bash
make: msgfmt: No such file or directory
```

In this case install the `gettext` package from your distribution's repository.


## Bug Reporting

Bugs should be reported to the Github bug tracker [https://github.com/micheleg/dash-to-dock/issues](https://github.com/micheleg/dash-to-dock/issues).

## License
Dash to Dock Gnome Shell extension is distributed under the terms of the GNU General Public License,
version 2 or later. See the COPYING file for details.
