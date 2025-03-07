---
title: into binary
categories: |
  conversions
version: 0.75.0
conversions: |
  Convert value to a binary primitive
usage: |
  Convert value to a binary primitive
---

# <code>{{ $frontmatter.title }}</code> for conversions

<div class='command-title'>{{ $frontmatter.conversions }}</div>

## Signature

```> into binary ...rest```

## Parameters

 -  `...rest`: for a data structure input, convert data at the given cell paths

## Examples

convert string to a nushell binary primitive
```shell
> 'This is a string that is exactly 52 characters long.' | into binary
```

convert a number to a nushell binary primitive
```shell
> 1 | into binary
```

convert a boolean to a nushell binary primitive
```shell
> true | into binary
```

convert a filesize to a nushell binary primitive
```shell
> ls | where name == LICENSE | get size | into binary
```

convert a filepath to a nushell binary primitive
```shell
> ls | where name == LICENSE | get name | path expand | into binary
```

convert a decimal to a nushell binary primitive
```shell
> 1.234 | into binary
```
