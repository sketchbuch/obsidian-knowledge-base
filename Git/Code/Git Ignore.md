# Git Ignore

Information about .gitgnore and ignore [patterns](https://github.com/git/git/blob/1a58bad0144dedd59eeef29b7ba7791aed19106f/Documentation/gitignore.txt#L70).

---

## Slashes

`/dir` will match a file or folder called `dir`
`/dir/` will match a folder named `dir`
`/dir/*` will match all files, directories and anything else inside a directory named `dir` (but not the `dir` directory itself).

[Source](https://stackoverflow.com/questions/17888695/difference-between-gitignore-rules-with-and-without-trailing-slash-like-dir-an)