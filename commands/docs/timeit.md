---
title: timeit
categories: |
  debug
version: 0.88.0
debug: |
  Time the running time of a block.
usage: |
  Time the running time of a block.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for debug

<div class='command-title'>{{ $frontmatter.debug }}</div>

## Signature

```> timeit {flags} (command)```

## Parameters

 -  `command`: the command or block to run


## Input/output types:

| input   | output   |
| ------- | -------- |
| any     | duration |
| nothing | duration |
## Examples

Times a command within a closure
```nu
> timeit { sleep 500ms }

```

Times a command using an existing input
```nu
> http get https://www.nushell.sh/book/ | timeit { split chars }

```

Times a command invocation
```nu
> timeit ls -la

```
