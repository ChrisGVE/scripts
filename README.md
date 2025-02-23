# scripts

## brew-upgrade

This script will update the brew registry, then upgrade all installed formulaes. It will then proceed with updating all outdated casks, doing it in a greedy manner such that it will even update applications which are self updating.

## convert-to-submodule

This script will create a git submodule for an individual `.config` subfolder. For instance if there is a `.config/nvim` configuration folder, by calling the script with `convert-to-submodule nvim` it will convert the `nvim` into its own repository within `.config`. Requirement: `config.<folder>` must exist in github.

## fzf-preview.sh

This is the script used to leverage on `bat` when using `fzf`.

## make_md

This script when run from inside a folder, say `project_x`, will create a markdown file called `project_x.md` that will contain all file prescribed, it is a recursive script.

Usage

```bash
make_md <list of extensions> [-exclude] | [+include]
```

When invoked with `make_md lua` it will collect all lua files within the markdown file, the content of the lua file will be enclosed within ``` to show code block. Multiple extensions can be given.

If adding multiple `[-exclude]` this will exclude all the noted files (note they can be given including the relative path, or just a file name, in which case if multiple files have the same name they will be excluded).

Alternatively the script can be used with `[+include]` only and will only include those files (same comment as for the exclude option).

## nvim-switch

This script allows to maintain multiple installations of neovim.

## ollama-loader

This script allows to pull multiple quantized version of a model. For instance `ollama-loader "qwen2.5-coder:0.5b-instruct[q6_K,fp16,q8_0]` will load all quantization in bracket, several models can be provided with their quantizations.

## symlink_all

This script is invoked with `symlink_all <source> <target>` and will create a symlink in `<target>` for all files in `<source>`.

## tat

This script will attach or create a tmux session named the same as the current directory.
