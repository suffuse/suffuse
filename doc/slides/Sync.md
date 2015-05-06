# Suffuse Synchronization

--

## Synchronization awareness
- synchronizing files across multiple machines
- it's a problem everyone has
- hard to imagine anyone's entirely satisfied
- Dropbox has vastly improved things, but not enough
- ever try to share a large media archive?
- say 50 GB of pictures with your spouse

--

## Smart files
- what if a file "knew" it was being synchronized
- reads/writes to it are handled intelligently
- they can be delayed under synchronization lock
- they can raise the file's sync priority
- why have an arbitrary sync order preference?

--

## Conflict resolution
- With [typed files](Typed.md) conflict resolution improves
- painful unsophistication of current solutions
- Dropbox: ```file.txt (Bob's conflicted copy 2015-04-01)```
- always data loss anxiety accompanies synchronization
- Pervasive revision control and typed files can change that

--

## Implementations of note
- [syncthing](https://github.com/syncthing/syncthing/)
- [unison](https://www.cis.upenn.edu/~bcpierce/unison/)
