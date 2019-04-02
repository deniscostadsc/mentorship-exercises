# lsuper

## Goal

Implement a simple `ls`-like command.

## Learning

- Standart library in one language
- OS basic structure
- SOLID
- Recursion
- Tests

## Interactions

I recommend to suggest a limited number of steps on each mentorship session.
This will help mentee to implement using SOLID if mentee is not used to SOLID
yet.

I also recommend enforce the use of tests.

After the first steps are finished. mentor must look at the code and give all
feedbacks to improve the code, explaining each point and with good resource to
go deep on that subject.

## Implementation

This implementation os `ls`, must have this features:

- If the folder is empty, a blank line must be printed.
- If there are files on folder, they must be printed in alphabetic order, as
follows:

```
$ lsuper
file1
file2
file3
```

- If there are folders on folder, they must be printed in alphabetic order and
with slashes in the and of the name, as can be seen below.

```
$ lsuper
dir1/
dir2/
dir3/
```

- If both, files and folders, exist, they must be printed with folders on top
of files. Within files, they must sorted alphabetically. Same for folders. A
sample can be seen below.

```
$ lsuper
dir1/
dir2/
dir3/
file1
file2
file3
```

- If a flag `--recursive` is passed to the `lsuper`, files and folders must be
printed recursivelly, with two spaces in front of the files every time it
enters a folder. A sample can be seen bellow.

```
$ lsuper --recursive
dir1/
  subdir1/
  subdir2/
    subdir1/
    subfile1
  subfile1
  subfile2
dir2/
  subdir1/
  subfile1
dir3/
file1
file2
file3
```

- If a flag `--format=spaces` is passed to the `lsuper`, the files/foldersmust
be printed with the default format, using spaces.

- If a flag `--format=tree` is passed to the `lsuper`, the files/folders must
be printed following `tree` command format. A sampla can be seen bellow.

```
lsuper --format=tree
.
├── dir1
├── dir2
├── dir3
├── file1
├── file2
└── file3
```

- Format flags (`--format[spaces,tree]`) and `--recursive` flag can be
combined. A sample can be seen below.

```
lsuper --format=tree --recursive
.
├── dir1
│   ├── subdir1
│   ├── subdir2
│   │   ├── subdir1
│   │   └── subfile1
│   ├── subfile1
│   └── subfile2
├── dir2
│   ├── subdir1
│   └── subfile1
├── dir3
├── file1
├── file2
└── file3

$ lsuper --format=spaces --recursive
dir1/
  subdir1/
  subdir2/
    subdir1/
    subfile1
  subfile1
  subfile2
dir2/
  subdir1/
  subfile1
dir3/
file1
file2
file3
```

## Problem extensions
If the mentee solves the problem quickly/easily additional features can be
added, like:

- Append `*` to files/folder with execution permission.
- Add new format, e.g. Json, XML.
