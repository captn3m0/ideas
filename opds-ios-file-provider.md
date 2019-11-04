# iOS OPDS File Provider

iOS 11 and above support browsing arbitary "cloud" filesystems using a ["File Provider Extension"][fpe]. This allows your application to expose a arbitary directory structure to other applications using the Files app (and file-picker dialogs).

Common use-cases include picking files from Dropbox, GDrive, iCloud etc. Here's a simple tutorial that demonstrates the idea: https://www.raywenderlich.com/697468-ios-file-provider-extension-tutorial.

The idea is to build a simple app that implements a dumb OPDS browser, along with a File Provider Extension. This magically makes all applications on your device OPDS aware, which is a Great Thing :tm:

OPDS here is the [open publication distribution system](https://en.wikipedia.org/wiki/OPDS), which allows a large number of clients to access digital libraries and publications with mostly-sane distribution and browsing semantics.

As an example, [Arxiv has a OPDS](https://arxiv-opds.herokuapp.com/) server without any authentication. You could enter this one URL in your application settings, and now all Arxiv PDFs are instantly browseable in your Files application.

OPDS support search as well, but I'm not sure of File Provider Extension does, but that would be another cool usecase. The application UI is just 2 screens:

1. List of connected OPDS Servers
2. Edit/Add screen for a OPDS Server. Includes fields for URL/Username/Password.

Brownie points for adding support for rendering ebook thumbnails, but that is optional.

## iOS \*sonic File Provider

Similarly, the [SubSonic API](http://www.subsonic.org/pages/api.jsp) is decently documented, reversed and re-implemented across a lot of clients. A single application that adds support for SubSonic File Provider will allow any other application to pick song files from a subsonic source. Not as many usecases as picking ebooks or PDFs, but good nonetheless.

[fpe]: https://developer.apple.com/documentation/fileprovider