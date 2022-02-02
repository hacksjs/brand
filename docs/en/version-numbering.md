# Version numbering

Version numbers for Hacks.js brand artwork loosely follow the [Semantic Versioning](http://semver.org) convention.

```txt
v[major].[minor].[patch]
```

- The `[major]` number is bumped to reflect material changes to the Hacks.js brand identity, or when existing graphics files are deleted.
- The `[minor]` number is bumped when new versions of the graphics are released, for example in new file formats, dimensions or sizes.
- The `[patch]` number is bumped when minor edits are made to existing graphics files, which do not change the visual presentation of the images (eg their rendered size).

A "breaking change" happens when a URL to a raw image file on GitHub — such as the following URL — returns an image that has _noticeably_ different rendering from its previous version. This MUST trigger a major version bump.

```txt
https://raw.githubusercontent.com/hacksjs/brand/latest/release/dist/hacksjs-logomark--100x100.svg
```

We don't use pre-release suffixes (eg `-beta.0`). However, "version zero" (`v0.x.x`) is considered a pre-release line.
