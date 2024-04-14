# none-ls-extras.nvim

Extra sources for [none-ls-extras.nvim](https://github.com/nvimtools/none-ls-extras.nvim)
for [nvimtools/none-ls.nvim](https://github.com/nvimtools/none-ls.nvim).

## 📦 Installation

This should be used as a dependency of **none-ls.nvim**.

### [lazy.nvim](https://github.com/folke/lazy.nvim)

```lua
  {
    "nvimtools/none-ls.nvim",
    dependencies = {
      "nvimtools/none-ls-extras.nvim",
      "zhaozg/none-ls-extras.nvim",
    },
  }
```

## Setup

Follow the steps in null-ls [setup](https://github.com/nvimtools/none-ls.nvim?tab=readme-ov-file#setup) section.

```lua
local null_ls = require("null-ls")

null_ls.setup {
    sources = {
        -- in zhaozg/none-ls-extras.nvim
        require("none-ls.diagnostics.luacheck"),
        require("none-ls.diagnostics.shellcheck"),
        require("none-ls.code_actions.shellicheck"),
        -- in nvimtools/none-ls-extras.nvim
        require("none-ls.diagnostics.cpplint"),
        require("none-ls.formatting.jq"),
        require("none-ls.code_actions.eslint"),
        ...
    }
}
```

Use `require("none-ls.METHOD.TOOL")` instead of `null_ls.builtins.METHOD.TOOL` to use these extras.

## Include Projects

- [none-ls-luacheck.nvim](https://github.com/gbprod/none-ls-luacheck.nvim)
- [none-ls-shellcheck.nvim](https://github.com/gbprod/none-ls-shellcheck.nvim)

## Related projects

You can search for sources via the [`none-ls-sources` topic](https://github.com/topics/none-ls-sources).

- [none-ls.nvim](https://github.com/nvimtools/none-ls.nvim)
- [none-ls-extras.nvim](https://github.com/nvimtools/none-ls-extras.nvim)
