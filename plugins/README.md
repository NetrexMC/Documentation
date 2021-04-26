# Plugins

Plugins are based on [FFI](https://en.wikipedia.org/wiki/Foreign_function_interface) (Foreign Function Interface) OR [NPP]() (Netrex Plugin Protocol).

## Table of Contents

- [FAQ](#faq) - Frequently asked questions
- [??](??) - nullptr

## FAQ

### How can I ensure my plugin doesn't have a virus?

The simple answer is, you can't. However I urge you to keep reading. While Netrex can't specifically identify a "threat" from a plugin that is **compiled**.  Netrex **CAN** assume that all *npp* (Netrex Plugin Protocol) are safe. Netrex will only be able to *read* data from the header included in the *npp* file if the protocol matches Netrex's. However this also means your plugins are more prune to breaking, which we will go over later.

### Can I use source files for plugins?

Theoretically, yes, but at the moment, no. Rust isn't interpreted (it can be, but this is for later), it's compiled. This means you would need to make a plugin that compiles your rust code (or any desired language) into a compiled binary, that you can then load using the plugin protocol.

