codefmt is a utility for syntax-aware code formatting. It contains several
built-in formatters, and allows new formatters to be registered by other
plugins.

# Supported file types

-   [Python](https://www.python.org/)
    -   [AutoPEP8](https://github.com/hhatto/autopep8)
    -   [Black](https://github.com/psf/black)
    -   [Isort](https://github.com/PyCQA/isort)
    -   [YAPH](https://github.com/google/yapf)
-   [Haskell](https://www.haskell.org/)
    -   [Brittany](https://github.com/lspitzner/brittany)
    -   [Hindent](https://github.com/mihaimaruseac/hindent)
-   [Bazel](https://docs.bazel.build/versions/main/user-manual.html)
    -   [Buildifier](https://github.com/bazelbuild/buildifier)
-   [C](https:////en.wikipedia.org/wiki/C_%28programming_language%29)
    -   [Clang-format](https://clang.llvm.org/docs/ClangFormat.html)
-   [C++](https://en.wikipedia.org/wiki/C%2B%2B)
    -   [Clang-format](https://clang.llvm.org/docs/ClangFormat.html)
-   [Java](https://www.java.com/)
    -   [Clang-format](https://clang.llvm.org/docs/ClangFormat.html)
    -   [Google-java-format](https://github.com/google/google-java-format)
-   [JavaScript](https://www.javascript.com/)
    -   [Clang-format](https://clang.llvm.org/docs/ClangFormat.html)
    -   [JS-beautify](https://github.com/beautify-web/js-beautify)
    -   [Prettier](https://github.com/prettier/prettier)
-   [JSON](https://en.wikipedia.org/wiki/JSON)
    -   [Clang-format](https://clang.llvm.org/docs/ClangFormat.html)
    -   [Prettier](https://github.com/prettier/prettier)
-   [Objective-C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html)
    -   [Clang-format](https://clang.llvm.org/docs/ClangFormat.html)
-   [Protobuf](https://github.com/protocolbuffers/protobuf)
    -   [Clang-format](https://clang.llvm.org/docs/ClangFormat.html)
-   [C#](https://docs.microsoft.com/en-us/dotnet/csharp/)
    -   [Clang-format](https://clang.llvm.org/docs/ClangFormat.html)
-   [Clojure](https://clojure.org/)
    -   [Cljstyle](https://github.com/greglook/cljstyle)
    -   [ZPrint](https://github.com/kkinnear/zprint)
-   [Cmake](https://cmake.org/)
    -   [Cmake-format](https://github.com/cheshirekow/cmake_format)
-   [Dart](https://dart.dev/)
    -   [Dartfmt](https://dart.dev/tools/dart-format)
-   [FISH](https://github.com/fish-shell/fish-shell)
    -   [Fish_indent](https://fishshell.com/docs/current/cmds/fish_indent.html)
-   [GN](https://chromium.googlesource.com/chromium/src/tools/gn/+/48062805e19b4697c5fbd926dc649c78b6aaa138/README.md)
    -   [Gn](https://gn.googlesource.com/gn/+/refs/heads/main/docs/reference.md)
-   [Go](https://go.dev/)
    -   [Gofmt](https://pkg.go.dev/cmd/gofmt)
-   [CSS](https://en.wikipedia.org/wiki/CSS)
    -   [JS-beautify](https://github.com/beautify-web/js-beautify)
    -   [Prettier](https://github.com/prettier/prettier)
-   [SASS](https://sass-lang.com/)
    -   [JS-beautify](https://github.com/beautify-web/js-beautify)
-   [SCSS](https://github.com/TryKickoff/scss)
    -   [JS-beautify](https://github.com/beautify-web/js-beautify)
    -   [Prettier](https://github.com/prettier/prettier)
-   [LESS](https://lesscss.org/)
    -   [JS-beautify](https://github.com/beautify-web/js-beautify)
    -   [Prettier](https://github.com/prettier/prettier)
-   [HTML](https://en.wikipedia.org/wiki/HTML)
    -   [JS-beautify](https://github.com/beautify-web/js-beautify)
    -   [Prettier](https://github.com/prettier/prettier)
-   [Kotlin](https://kotlinlang.org/)
    -   [Ktfmt](https://github.com/facebookincubator/ktfmt)
-   [Lua](https://www.lua.org/)
    -   [LuaFormatterFiveOne](https://github.com/LuaDevelopmentTools/luaformatter)
-   [Nix](https://nixos.wiki/wiki/Nix_Expression_Language)
    -   [Nixpkgs-fmt](https://github.com/nix-community/nixpkgs-fmt)
-   [OCaml](https://ocaml.org/)
    -   [OCamlformat](https://github.com/ocaml-ppx/ocamlformat)
-   [Markdown](https://en.wikipedia.org/wiki/Markdown)
    -   [Prettier](https://github.com/prettier/prettier)
-   [YAML](https://yaml.org/)
    -   [Prettier](https://github.com/prettier/prettier)
-   [JSX](https://reactjs.org/docs/introducing-jsx.html)
    -   [Prettier](https://github.com/prettier/prettier)
-   [MDX](https://mdxjs.com/)
    -   [Prettier](https://github.com/prettier/prettier)
-   [Vue](https://vuejs.org/)
    -   [Prettier](https://github.com/prettier/prettier)
-   [Ruby](https://www.ruby-lang.org/)
    -   [Rubocop](https://github.com/rubocop/rubocop)
-   [Rust](https://www.rust-lang.org/)
    -   [Rustfmt](https://github.com/rust-lang/rustfmt)
-   [Sh](https://en.wikipedia.org/wiki/Shell_script)
    -   [Shfmt](https://github.com/mvdan/sh)
-   [Bash](https://www.gnu.org/software/bash/)
    -   [Shfmt](https://github.com/mvdan/sh)
-   [Mksh](http://www.mirbsd.org/mksh.htm)
    -   [Shfmt](https://github.com/mvdan/sh)

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
