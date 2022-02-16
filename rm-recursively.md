## Delete all files of a specific name in the current directory recursively 

If your current directory is `~/dir1/` and you want to find all files that are called `something.bak`,
even if they are in `~/dir1/dir2/dir3/`, then you should run this command:

```sh
find . -name "*.bak" -type f
```

> take for granted that you all understand that with `something.bak` I mean any file with the extension `.bak` :)

Now that you checked all the files that are called like that, you can delete them all with adding the option `-delete`, just this way:

```sh
find . -name "*.bak" -type f -delete
```

> Note: I recommend to use this command with precaution. With the first command you check the files you are about to delete.
> Also, make sure that `-delete` is the last argument in your command. If you put it before `-name *.bak`, *it will delete everything*.
