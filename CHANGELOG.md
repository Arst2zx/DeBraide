# Changelog

## Release v1.0.0

- Add tempFile static method that allows to open temporary files.
- Remove deprecated `execute` method.
  Use [TheProcess](https://code.dlang.org/packages/theprocess) instead

---

## Release v0.1.7

- Added new param to `Path.parent` method - `absolute`, that is by default set to `true` (to keep backward compatibility).
  If this param is set to `false`, then path will not be converted to absolute path before computing parent path,
  thus it will be possible to get non-absolute parent path from non-absolute path.
  For example:

  ```d
  Path("parent", "child").parent == Path.current.join("parent");
  Path("parent", "child").parent(false) == Path("parent");
  ```
