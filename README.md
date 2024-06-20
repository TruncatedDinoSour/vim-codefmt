# This repository has been migrated to the self-hosted ari-web Forgejo instance: <https://git.ari.lt/ari/vim-codefmt>
codefmt is a utility for syntax-aware code formatting. It contains several
built-in formatters, and allows new formatters to be registered by other
plugins.

# Supported file types

-   [Python](https://www.python.org/)
    -   [AutoPEP8][]
    -   [Black][]
    -   [Isort][]
    -   [YAPH][]
-   [Haskell](https://www.haskell.org/)
    -   [Brittany][]
    -   [Hindent][]
-   [Bazel](https://docs.bazel.build/versions/main/user-manual.html)
    -   [Buildifier][]
-   [C](https:////en.wikipedia.org/wiki/C_%28programming_language%29)
    -   [Clang-format][]
-   [C++](https://en.wikipedia.org/wiki/C%2B%2B)
    -   [Clang-format][]
-   [Java](https://www.java.com/)
    -   [Clang-format][]
    -   [Google-java-format](https://github.com/google/google-java-format)
-   [JavaScript](https://www.javascript.com/)
    -   [Clang-format][]
    -   [JS-beautify][]
    -   [Prettier][]
-   [JSON](https://en.wikipedia.org/wiki/JSON)
    -   [Clang-format][]
    -   [Prettier][]
-   [Objective-C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html)
    -   [Clang-format][]
-   [Protobuf](https://github.com/protocolbuffers/protobuf)
    -   [Clang-format][]
-   [C#](https://docs.microsoft.com/en-us/dotnet/csharp/)
    -   [Clang-format][]
-   [Clojure](https://clojure.org/)
    -   [Cljstyle][]
    -   [ZPrint][]
-   [Cmake](https://cmake.org/)
    -   [Cmake-format][]
-   [Dart](https://dart.dev/)
    -   [Dartfmt][]
-   [FISH](https://github.com/fish-shell/fish-shell)
    -   [Fish_indent][]
-   [GN](https://chromium.googlesource.com/chromium/src/tools/gn/+/48062805e19b4697c5fbd926dc649c78b6aaa138/README.md)
    -   [Gn][]
-   [Go](https://go.dev/)
    -   [Gofmt][]
-   [CSS](https://en.wikipedia.org/wiki/CSS)
    -   [JS-beautify][]
    -   [Prettier][]
-   [SASS](https://sass-lang.com/)
    -   [JS-beautify][]
-   [SCSS](https://github.com/TryKickoff/scss)
    -   [JS-beautify][]
    -   [Prettier][]
-   [LESS](https://lesscss.org/)
    -   [JS-beautify][]
    -   [Prettier][]
-   [HTML](https://en.wikipedia.org/wiki/HTML)
    -   [JS-beautify][]
    -   [Prettier][]
-   [Kotlin](https://kotlinlang.org/)
    -   [Ktfmt][]
-   [Lua](https://www.lua.org/)
    -   [LuaFormatterFiveOne][]
-   [Nix](https://nixos.wiki/wiki/Nix_Expression_Language)
    -   [Nixpkgs-fmt][]
-   [OCaml](https://ocaml.org/)
    -   [OCamlformat][]
-   [Markdown](https://en.wikipedia.org/wiki/Markdown)
    -   [Prettier][]
-   [YAML](https://yaml.org/)
    -   [Prettier][]
-   [JSX](https://reactjs.org/docs/introducing-jsx.html)
    -   [Prettier][]
-   [MDX](https://mdxjs.com/)
    -   [Prettier][]
-   [Vue](https://vuejs.org/)
    -   [Prettier][]
-   [Ruby](https://www.ruby-lang.org/)
    -   [Rubocop][]
-   [Rust](https://www.rust-lang.org/)
    -   [Rustfmt][]
-   [Sh](https://en.wikipedia.org/wiki/Shell_script)
    -   [Shfmt][]
-   [Bash](https://www.gnu.org/software/bash/)
    -   [Shfmt][]
-   [Mksh](http://www.mirbsd.org/mksh.htm)
    -   [Shfmt][]
-   [TypeScript](https://www.typescriptlang.org/)
    -   [Clang-format][]

[clang-format]: https://clang.llvm.org/docs/ClangFormat.html
[shfmt]: https://github.com/mvdan/sh
[rustfmt]: https://github.com/rust-lang/rustfmt
[rubocop]: https://github.com/rubocop/rubocop
[prettier]: https://github.com/prettier/prettier
[ocamlformat]: https://github.com/ocaml-ppx/ocamlformat
[nixpkgs-fmt]: https://github.com/nix-community/nixpkgs-fmt
[luaformatterfiveone]: https://github.com/LuaDevelopmentTools/luaformatter
[ktfmt]: https://github.com/facebookincubator/ktfmt
[js-beautify]: https://github.com/beautify-web/js-beautify
[gofmt]: https://pkg.go.dev/cmd/gofmt
[gn]: https://gn.googlesource.com/gn/+/refs/heads/main/docs/reference.md
[autopep8]: https://github.com/hhatto/autopep8
[black]: https://github.com/psf/black
[isort]: https://github.com/PyCQA/isort
[yaph]: https://github.com/google/yapf
[fish_indent]: https://fishshell.com/docs/current/cmds/fish_indent.html
[dartfmt]: https://dart.dev/tools/dart-format
[cmake-format]: https://github.com/cheshirekow/cmake_format
[cljstyle]: https://github.com/greglook/cljstyle
[zprint]: https://github.com/kkinnear/zprint
[brittany]: https://github.com/lspitzner/brittany
[hindent]: https://github.com/mihaimaruseac/hindent
[buildifier]: https://github.com/bazelbuild/buildifier

# Commands

Use `:FormatLines` to format a range of lines or use `:FormatCode` to format
the entire buffer. Use `:NoAutoFormatBuffer` to disable current buffer
formatting.

# Usage example

Before:

```c
int foo(int * x) { return * x** x ; }
```

After running `:FormatCode`:

```c
int foo(int* x) { return *x * *x; }
```

# Installation

_These are only few examples_

## [Vundle](https://github.com/VundleVim/Vundle.vim)

```vim
call vundle#begin()
" ...

" Add maktaba and codefmt to the runtimepath.
" (The latter must be installed before it can be used.)
Plugin 'google/vim-maktaba'
Plugin 'TruncatedDinosour/vim-codefmt'

" ...
call vundle#end()
```

## [NeoBundle](https://github.com/Shougo/neobundle.vim)

```vim
call neobundle#begin(expand('...'))
" ...

" Add maktaba and codefmt to the runtimepath.
" (The latter must be installed before it can be used.)
NeoBundle 'google/vim-maktaba'
NeoBundle 'TruncatedDinosour/vim-codefmt'

" ...
call neobundle#end()
```

## [VimPlug](https://github.com/junegunn/vim-plug)

```vim
" Add maktaba and codefmt to the runtimepath.
" (The latter must be installed before it can be used.)
call plug#begin("...")
" ...

Plug 'google/vim-maktaba'
Plug 'TruncatedDinosour/vim-codefmt'

" ...
call plug#end()
```

# [Pathogen](https://github.com/tpope/vim-pathogen)

```sh
$ cd ~/.vim/bundle
$ git clone https://github.com/google/vim-maktaba
$ git clone https://github.com/TruncatedDinosour/vim-codefmt
```

Make sure you have updated maktaba recently. Codefmt depends upon maktaba
to register formatters.

# Autoformatting

Want to just sit back and let autoformat happen automatically? Add this to your
`vimrc` (or any subset):

```vim
autocmd FileType * silent FormatCode
```

# Configuring formatters

Most formatters have some options available that can be configured with variables
but you can also use [Glaive](https://github.com/google/vim-glaive)

You can get a quick view of all codefmt flags by executing `:Glaive codefmt`, or
start typing flag names and use tab completion. See `:help Glaive` for usage
details.

# Installing formatters

Codefmt defines several built-in formatters. The easiest way to see the list of
available formatters is via tab completion: Type `:FormatCode <TAB>` in vim.
Formatters that apply to the current filetype will be listed first.

To use a particular formatter, type `:FormatCode FORMATTER-NAME`. This will
either format the current buffer using the selected formatter or show an error
message with basic setup instructions for this formatter. Normally you will
trigger formatters via key mappings and/or autocommand hooks. See
vroom/main.vroom to learn more about formatting features, and see
vroom/FORMATTER-NAME.vroom to learn more about usage for individual formatters.

## Creating a New Formatter

Assume a filetype `myft` and a formatter called `MyFormatter`.

-   Create a new file in `autoload/codefmt/myformatter.vim` See
    `autoload/codefmt/buildifier.vim for an example. This is where all the
    logic for formatting goes.

-   Register the formatter in
    [plugin/register.vim](plugin/register.vim)
    with:

    ```vim
    call s:registry.AddExtension(codefmt#myformatter#GetFormatter())
    ```

-   Create a flag in
    [instant/flags.vim](instant/flags.vim)

    ```vim
    ""
    " The path to my formatter executable.
    call s:plugin.Flag('myformatter_executable', 'myformatter')
    ```

-   Update the README.md to mention your new filetype

Thats it! Now make a pull request.
