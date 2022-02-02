# Workflow

To release updated versions or formats of the Hacks.js logo or related brand artwork, follow these steps:

1.  Checkout the `latest/release` branch.

2.  Makes changes to the contents of the `dist` directory as required.

    _Note: Master files for our logos and other brand graphics are kept in a separate private repository. The built, distributable artifacts are copied to this repository for public release._

3.  Commit your changes.

    ```sh
    $ git commit -a -m "Add more PNG variations"
    ```

4.  Update the CHANGELOG, bumping the version number as per our [version numbering](version-numbering.md) policy. Use `git log` to see a list of commits since the last release, and use the commit messages as a basis for the contents of the CHANGELOG entry.
  
    Commit the change to the CHANGELOG with the message "v[major].[minor].[patch]".

    ```sh
    $ git commit -a -m "v2.3.11"
    ```

5.  Push the commits to the upstream [reference repository](https://github.com/hacksjs/brand).

    ```sh
    $ git push (origin latest/release)
    ```

6.  Create an annotated tag against the last commit, also with the message "v[major].[minor].[patch]"
  
    ```sh
    $ git tag -a v2.3.11 -m "v2.3.11"
    ```

7.  Push this new tag upstream.

    ```sh
    $ git push origin v2.3.11
    ```

    Or, push all tags to the remote server that are not already there:

    ```sh
    $ git push --tags
    ```

8.  On GitHub, choose to [create a new release](https://github.com/hacksjs/brand/releases/new), then:

    - Select the new tag as the target for the release.
    - The release name must in the format "v[major].[minor].[patch]", eg "v2.3.11".
    - The description can be copied from the CHANGELOG.
    - Tick the "pre-release" box only for version zero (`v0.x.x`) releases.

    GitHub will make the release available as a downloadable archive file.
