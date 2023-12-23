# $name$

## Compile

Assuming Agda is available (see Installation section),
```bash
agda --compile $filename$.agda
```

The `--compile` flag creates via the GHC backend a binary file in the top-level folder that can be executed:
```bash
./$filename$
```

## Installation

If using [nix](https://nixos.org/), a [shell.nix](shell.nix) file is provided as part of the repo that will make Agda and it's standard library available in a ephemeral nix shell. Just `cd` into the project and type 
```bash
nix-shell
```
The same can be automated using `direnv`. 

See [official guide](https://agda.readthedocs.io/en/latest/getting-started/installation.html) for other installation options. 

## CI/CD 

This project uses github actions to ensure at every commit the agda files are compiled. 
