---
title: help modules
categories: |
  core
version: 0.88.0
core: |
  Show help on nushell modules.
usage: |
  Show help on nushell modules.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for core

<div class='command-title'>{{ $frontmatter.core }}</div>

## Signature

```> help modules {flags} ...rest```

## Flags

 -  `--find, -f {string}`: string to find in module names and usage

## Parameters

 -  `...rest`: the name of module to get help on


## Input/output types:

| input   | output |
| ------- | ------ |
| nothing | table  |

## Examples

show all modules
```nu
> help modules

```

show help for single module
```nu
> help modules my-module

```

search for string in module names and usages
```nu
> help modules --find my-module

```

## Notes
When requesting help for a single module, its commands and aliases will be highlighted if they
are also available in the current scope. Commands/aliases that were imported under a different name
(such as with a prefix after `use some-module`) will be highlighted in parentheses.