# pages-test

Notes to self. This is not useful for public consumption.

Workaround to test various github sites before merging to master. Needed since I miserably failed to install a local Jekyll server.

Under sites are the sites to be tested. Copy the contents of any subdirectory to `docs` and push to master in order to to see the site at https://marcverhagen.github.io/pages-test/.

So far only used for experimenting with the MMIF specifications site at https://github.com/clamsproject/mmif. To do that you would copy the contents of the `docs` directory in that site to `docs` in this repository. To make it work you would have to edit `docs/_config.yml` and replace


```
url: "https://mmif.clams.ai"
baseurl: ""
```

with

```
url: "https://marcverhagen.github.io"
baseurl: "/pages-test"
```

You can park work in `sites/mmif` if you want.
