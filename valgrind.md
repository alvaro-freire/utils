### Valgrind command

This tool is very useful to check memory leaks problems in your code.
Here you have the command I normally use:

```sh
valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes --verbose --log-file=log.txt ./program
```

> Note: if your program is "main", then your command should end up with ./main instead of ./program
