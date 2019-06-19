# Check out the git repository

```
git clone --recursive git@gitlab.physik.uni-muenchen.de:Nikolai.Hartmann/erum-data-website.git
```

# Get Hugo

Either install for your favorite distribution or just get the all-in-one binary: https://github.com/gohugoio/hugo/releases

# Test/Develop website

You can start a hugo web server that on-the-fly build and deploys the website on your local machine:

```
cd erum-data-website
hugo server
```

# Build

To just build the static html content simply run `hugo` in the project
directory. The content is then available in the `public/` directory.

# Further information

- https://gohugo.io/documentation/
- https://themes.gohugo.io/

