# Local folders source

Declares the host-provided local-folder scanning capability. The Wasm module has no filesystem
access. Users can create any number of local source instances and attach any number of folders to
each instance; the host stores those memberships in the portable SQLite database.
