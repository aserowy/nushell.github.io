---
title: default
categories: |
  filters
version: 0.88.0
filters: |
  Sets a default row's column if missing.
usage: |
  Sets a default row's column if missing.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for filters

<div class='command-title'>{{ $frontmatter.filters }}</div>

## Signature

```> default {flags} (default value) (column name)```

## Parameters

 -  `default value`: the value to use as a default
 -  `column name`: the name of the column


## Input/output types:

| input | output |
| ----- | ------ |
| any   | any    |

## Examples

Give a default 'target' column to all file entries
```nu
> ls -la | default 'nothing' target

```

Get the env value of `MY_ENV` with a default value 'abc' if not present
```nu
> $env | get --ignore-errors MY_ENV | default 'abc'

```

Replace the `null` value in a list
```nu
> [1, 2, null, 4] | default 3
╭───┬───╮
│ 0 │ 1 │
│ 1 │ 2 │
│ 2 │ 3 │
│ 3 │ 4 │
╰───┴───╯

```
