---
title: from ssv
categories: |
  formats
version: 0.75.0
formats: |
  Parse text as space-separated values and create a table. The default minimum number of spaces counted as a separator is 2.
usage: |
  Parse text as space-separated values and create a table. The default minimum number of spaces counted as a separator is 2.
---

# <code>{{ $frontmatter.title }}</code> for formats

<div class='command-title'>{{ $frontmatter.formats }}</div>

## Signature

```> from ssv --noheaders --aligned-columns --minimum-spaces```

## Parameters

 -  `--noheaders`: don't treat the first row as column names
 -  `--aligned-columns`: assume columns are aligned
 -  `--minimum-spaces {int}`: the minimum spaces to separate columns

## Examples

Converts ssv formatted string to table
```shell
> 'FOO   BAR
1   2' | from ssv
```

Converts ssv formatted string to table but not treating the first row as column names
```shell
> 'FOO   BAR
1   2' | from ssv -n
```
