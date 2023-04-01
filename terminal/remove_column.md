## Remove specific column of csv from terminal

#### This removes the first column:

> Column    -> -f1
> Separator -> ';'

```sh
cut -d ';' -f1 --complement file.txt
```
