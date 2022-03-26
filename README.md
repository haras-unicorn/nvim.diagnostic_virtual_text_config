# `nvim.diagnostic_virtual_text_config`

![Showcase](assets/screenshot.png)

`nvim.diagnostic_virtual_text_config` is a `Neovim` plugin that lets you
configure the position, style, and display of diagnostic virtual text.

## Overview

LSPs provide lots of diagnostics for code (typically: errors, warnings,
linting). By default, they're displayed using virtual text at the end of the
line. This virtual text good enough in many cases, but it can often get
unwieldy. For example, when there are more than one diagnostic per line, it is
often impossible to read them all. Or when there's a very long diagnostic, it
is often impossible to read it all the way.

`nvim.diagnostic_virtual_text_config` seeks to solve this issue.

## Installation

Using `packer.nvim`:

```lua
use {
  "Hrle97/nvim.diagnostic_virtual_text_config",
  config = function()
    require("nvim.diagnostic_virtual_text_config").setup {
      -- your config here...
    }
  end,
}
```

`nvim.diagnostic_virtual_text_config` removes the default diagnostic virtual
text by default, and replaces it with virtual text that sits on top of each
diagnostic line.

## Configuration

Configuration, by popular convention, is done by calling the `setup` function
like so:

```lua
require("nvim.diagnostic_virtual_text_config").setup {
  -- your config here...
}
```

## Attributions

This plugin is a fork of `https://git.sr.ht/~whynothugo/lsp_lines.nvim` by 
Hugo Osvaldo Barrera.
