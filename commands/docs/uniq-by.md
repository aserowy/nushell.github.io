---
title: uniq-by
categories: |
  filters
version: 0.88.0
filters: |
  Return the distinct values in the input by the given column(s).
usage: |
  Return the distinct values in the input by the given column(s).
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for filters

<div class='command-title'>{{ $frontmatter.filters }}</div>

## Signature

```> uniq-by {flags} ...rest```

## Flags

 -  `--count, -c`: Return a table containing the distinct input values together with their counts
 -  `--repeated, -d`: Return the input values that occur more than once
 -  `--ignore-case, -i`: Ignore differences in case when comparing input values
 -  `--unique, -u`: Return the input values that occur once only

## Parameters

 -  `...rest`: the column(s) to filter by


## Input/output types:

| input     | output    |
| --------- | --------- |
| list\<any\> | list\<any\> |
| table     | table     |
## Examples

Get rows from table filtered by column uniqueness
```nu
> [[fruit count]; [apple 9] [apple 2] [pear 3] [orange 7]] | uniq-by fruit
╭───┬────────┬───────╮
│ # │ fruit  │ count │
├───┼────────┼───────┤
│ 0 │ apple  │     9 │
│ 1 │ pear   │     3 │
│ 2 │ orange │     7 │
╰───┴────────┴───────╯

```
