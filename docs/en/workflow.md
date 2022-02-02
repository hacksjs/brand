# Workflow

To release updated versions or formats of the Hacks.js logo, or related brand artwork, follow these steps:

1.  Checkout the `latest/release` branch.

2.  Makes changes to the contents of the `dist` directory as required.

    _Note: master files for our logos and brand artifacts are kept in a separate private repository._

3.  Commit the changes, updating the CHANGELOG in the same commit.

4.  Create an annotated tag against the last commit, bumping the version number as per our [version numbering](version-numbering.md) policy:
  
    ```sh
    $ git tag -a v2.3.11 -m "v2.3.11"
    ```

5.  Push the changes, including the new tag, to the `latest/release` branch in the upstream [reference repository](//github.com/hacksjs/brand).

    ```sh
    $ git push --follow-tags
    ```
