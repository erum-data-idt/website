# Check out the git repository

```
git clone --recursive <this-repository>
```

# Update the repository

After updating the repository - e.g. with `git pull` - it might be nescessary to
run the following commands to update the submodules in the [themes](themes)
folder.

```
git submodule init
git submodule update
```

# Get Hugo

You need **Hugo v0.57.0** or newer. The easiest way is to just download the
latest all-in-one binary: https://github.com/gohugoio/hugo/releases/latest. On
Linux (64bit) choose `hugo_extended_<version>_Linux-64bit.tar.gz`.

# Test/Develop website

You can start a hugo web server that on-the-fly build and deploys the website on your local machine:

```
cd erum-data-website
hugo server
```

# Build

To just build the static html content simply run `hugo` in the project
directory. The content is then available in the `public/` directory.
To browse the files locally, set the `relativeURLS` option e.g. by building with

```
env HUGO_RELATIVEURLS=1  hugo
```

The build directory can be changed via `HUGO_PUBLISHDIR=path/to/build/dir`.

Example for a clean build and upload:

```
rm -r public
hugo
rsync -n -avr --delete public/ <webserver-url>:<webserver-path>/
```

When everything looks fine run the command without `-n` (dry-run)

# URLs

The website is available via
- https://www.erum-data-idt.de
- https://www.erum-data.de

# Further information

- https://gohugo.io/documentation/
- https://themes.gohugo.io/
- https://github.com/liwenyip/hugo-easy-gallery - for making image galleries
  (included in this repository)
