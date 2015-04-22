# Roadmap (not really)

--

## Components
- [bridj](https://github.com/nativelibs4java/BridJ) java FUSE bindings
- suffuse API simplifies FUSE
- suffuse library creates collections, typed I/O
- suffuse daemon (suffused) is sfs server

--

## Looking ahead
- Extended file attributes expose file types
- Using types effectively requires suffuse-aware shell
- And suffuse-aware programs, especially find, grep, etc
- With typed files, programs, and pipes, a new world
- Type-aware tab-completion anywhere in the pipeline
- typed logs, type-aware console formatting
- suffuse shell: shuffle?

--

## Known Unknowns
- Absolute paths. chroot to sfsImport("/") ?
- Notifications a mess, worse in java. [libuv](https://github.com/libuv/libuv)?
- Performance unworrisome but to be monitored
- Reliable/performant/portable notifications
- Reliable/performant/portable xattrs
- Underlying filesystem sabotage (e.g. case insensitivity)
