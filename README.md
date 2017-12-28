# `erc-status-sidebar`

[![MELPA](https://melpa.org/packages/erc-status-sidebar-badge.svg)](https://melpa.org/#/erc-status-sidebar)

A [hexchat](https://hexchat.github.io/)-like activity overview for ERC
channels. This an alternative view for the `erc-track` module. It
displays all the same information `erc-track` puts in the mode line, but
can be relegated to a single frame dedicated to IRC.

![Demo GIF of erc-status-sidebar](demo.gif)

## Installation

Fetch the `erc-status-sidebar.el` repository

```bash
git clone https://github.com/drewbarbs/erc-status-sidebar.git
```

Load it in your emacs init file

```el
(add-to-list 'load-path "/path/to/erc-status-sidebar")
(require 'erc-status-sidebar)
```

## Usage

To open the ERC status sidebar in the current frame use `M-x
erc-status-sidebar-open`. Ensure the `erc-track` module is active (a
member of `erc-modules`). This is the default setting for ERC.

To close the sidebar on the current frame use `M-x
erc-status-sidebar-close`. Provide a prefix argument to close the
sidebar on all frames.

To kill the sidebar buffer and close the sidebar on all frames, use
`M-x erc-status-sidebar-kill`.

## Configuration

To specify a list message types that *do not* update the status
sidebar (e.g. `JOIN` and `PART` messages), update the "Erc Track
Exclude Types" custom setting: `M-x customize-group <RET> erc-track`.

## Acknowledgments

Credit to [`sidebar.el`](https://github.com/sebastiencs/sidebar.el)
and [`outline-toc.el`](https://github.com/abingham/outline-toc.el),
from which all the sidebar window management ideas were lifted.

## License

[GNU General Public License v3](https://www.gnu.org/licenses/gpl-3.0.en.html)
