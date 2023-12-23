# Agda.g8

A [Giter8][g8] seed for **minimalist** agda projects.

## About the template

### Run

G8 integrates seemlessly with [sbt](https://www.scala-sbt.org/). Assuming `sbt` is available in the system, one way to generate a new Agda project with name `<name>` in a folder called `<name>` from this seed is

```bash
 sbt new git@github.com:alessandrocandolini/agda.g8.git --name=<name> --force
```

(Alternatively, there is also a stand-alone `g8` command-line which is more scala agnostic.)

`name` for now is the only supported template variable at the moment and it's used for both the `*.agda` main file as well as the folder name.

See http://www.foundweekends.org/giter8/usage.html#Usage for more details

### Features

* agda file that can be compiled with GHC backend
* nix-shell which includes also the standard library
* standard files (`README.md` with instructions, `.gitignore`)
* simple github actions to the generated project (using nix instead of [setup-agda](https://github.com/wenkokke/setup-agda) intentionally, to make local and remote behaviour consistent) 
* the template runs github actions itself, to check at least the trivial issues with the seed

### Todo

* import agdarsec in nix-shell and github actions
* add support for literate agda in latex conditionally
* add support for equational reasoning
* many other things

## About Giter8

### Install

One option is via [nix](https://nixos.org/), if available on the system:
```bash
nix-shell -p sbt
```

On MAC OS X, both `sbt` and `giter8` are available for example via the Homebrew package manager:
```
brew update
brew install sbt
brew install giter8
```

For more options, refer to the [original documentation](http://www.foundweekends.org/giter8/setup.html)

### Crash course

* Giter8 generates a project that has exactly the same structure of the [src/main/g8](src/main/g8) folder
* template variables are defined in the [default.properties](src/main/g8/default.properties) file
* template variables can be accessed as `$name of the variable$` (ie, between `$`) from everywhere (including path and filenames)
* `$` is the only reserved symbol. whenever you need to use a `$` for purposes other than referring to a template variable be sure to escape it as `\$`; this is a typical source of errors

A more comprehensive guide here: http://www.foundweekends.org/giter8/Contents+in+Depth.html

Template license
----------------
Written in 2023 by Alessandro Candolini (alessandro.candolini@gmail.com)
[other author/contributor lines as appropriate]

To the extent possible under law, the author(s) have dedicated all copyright and related
and neighboring rights to this template to the public domain worldwide.
This template is distributed without any warranty. See <https://creativecommons.org/publicdomain/zero/1.0/>.

[g8]: https://www.foundweekends.org/giter8/
