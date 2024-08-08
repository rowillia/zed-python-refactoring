# zed-python-refactoring
Adds refactoring support for Python in Zed

## Installation Steps

### Install the LSP

You can find the LSP implementation at [cst-lsp](https://github.com/rowillia/cst-lsp)

```bash
pip install cst-lsp
rustup target add wasm32-wasi
```

To make sure things are installed properly, run `cst_lsp --stdio`.
It should run without error (you'll have to Ctrl-C to kill it manually)


### Install Development Extension

1. Open Zed
2. ⌘+Shift+P - "zed: install dev extension"
3. Point to this directory

If things aren't working check out the logs with:

```bash
tail -f ~/Library/Logs/Zed/Zed.log
```

### Add as a language server
```json
{
  "languages": {
    "Python": {
      "language_servers": ["pyright", "python-refactoring"]
    }
  }
}
```

Once installed, you should see a code action to "Refactor" one you select some Python lines.
