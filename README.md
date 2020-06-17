## Boost Heap 1.65.1 BCP Dump

This is a dump of all the required Boost Headers to use [Boost Heap](https://www.boost.org/doc/libs/1_65_0/doc/html/heap.html) library in a standalone project.

This repository is suited for submodule inclusion in any git-based project.

The library has been used successfully in a project targeting RTEMS Real Time Embedded Operating System, whithout modifications from the BCP dump.

The BCP dump has been executed on an instance of Ubuntu 18.04, where Boost was installed from the official repositories.

You can obtain a dump like this using [BCP](https://www.boost.org/doc/libs/1_73_0/tools/bcp/doc/html/index.html) and excluding non-boost headers
(since you will use platform-provided equivalents, at least in a POSIX environment like RTEMS).

```
mkdir temp
bcp --boost=/usr/include heap ./temp
mkdir BoostHeap
mv ./temp/boost BoostHeap/
rm -rf temp
```

