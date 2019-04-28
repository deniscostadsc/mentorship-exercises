# lsimple

## Goal

Implement a simple `ls`-like command.

## Learning

- OS basic structure
- Recursion
- SOLID
- Standart library in one language
- Tests and TDD

## Implementation

This implementation os `ls`, must have this features:

- If the folder is empty, a blank line must be printed.
- If there are files on folder, they must be printed in alphabetic order, as
follows:

```
$ lsimple
file1
file2
file3
```

- If there are folders on folder, they must be printed in alphabetic order and
with slashes in the and of the name, as can be seen below.

```
$ lsimple
dir1/
dir2/
dir3/
```

- If both, files and folders, exist, they must be printed with folders on top
of files. Within files, they must sorted alphabetically. Same for folders. A
sample can be seen below.

```
$ lsimple
dir1/
dir2/
dir3/
file1
file2
file3
```

- If a flag `--recursive` is passed to the `lsimple`, files and folders must be
printed recursivelly, with two spaces in front of the files every time it
enters a folder. A sample can be seen bellow.

```
$ lsimple --recursive
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

- If a flag `--format=spaces` is passed to the `lsimple`, the files/foldersmust
be printed with the default format, using spaces.

- If a flag `--format=tree` is passed to the `lsimple`, the files/folders must
be printed following `tree` command format. A sampla can be seen bellow.

```
lsimple --format=tree
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
lsimple --format=tree --recursive
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

$ lsimple --format=spaces --recursive
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
