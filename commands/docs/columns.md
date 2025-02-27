---
title: columns
categories: |
  filters
version: 0.88.0
filters: |
  Given a record or table, produce a list of its columns' names.
usage: |
  Given a record or table, produce a list of its columns' names.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for filters

<div class='command-title'>{{ $frontmatter.filters }}</div>

## Signature

```> columns {flags} ```


## Input/output types:

| input  | output       |
| ------ | ------------ |
| record | list\<string\> |
| table  | list\<string\> |
## Examples

Get the columns from the record
```nu
> { acronym:PWD, meaning:'Print Working Directory' } | columns
╭───┬─────────╮
│ 0 │ acronym │
│ 1 │ meaning │
╰───┴─────────╯

```

Get the columns from the table
```nu
> [[name,age,grade]; [bill,20,a]] | columns
╭───┬───────╮
│ 0 │ name  │
│ 1 │ age   │
│ 2 │ grade │
╰───┴───────╯

```

Get the first column from the table
```nu
> [[name,age,grade]; [bill,20,a]] | columns | first

```

Get the second column from the table
```nu
> [[name,age,grade]; [bill,20,a]] | columns | select 1

```

## Notes
This is a counterpart to `values`, which produces a list of columns' values.