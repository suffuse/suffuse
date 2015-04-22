# Suffuse for Developers

--

## Rich source code
- SFS is staged metaprogramming minus stages
- always-on code generation to any depth
- a.conf -> b.sh -> C.scala
- a.json -> { a.java, a.scala, a.hs }

--

## Read/write in-memory data
- Any tree can be exposed as an SFS
- Any SFS is a tree of key/value pairs
- Given /s/foo exposing internal data
- ```Serialize: cp /s/foo.json bar```
- ```Deserialize: cp bar /s/foo.json```

--

## Infinite ivy/maven
 - Given an ivy/maven metadata index
 - Every file in the index is instantly visible
 - Reading a file triggers transparent download/cache
 - Filter to latest versions, specific cross-build, etc.
 - Publish by copying into the repository

--

## Test cases
 - scalac has hundreds of test cases involving multiple files
 - Multiple virtual files in a single file
 - J.java, S.scala, expected-output.txt, steps.cmd
