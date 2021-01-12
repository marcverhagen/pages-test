# pages-test

Workaround to test various github sites before merging to master. Needed since I miserably failed to install a recent local Jekyll server.

>  These are notes to self. Not really useful for public consumption.

Under `sites` are the sites to be tested. Copy the contents of any subdirectory to `docs` and push to master in order to to see the site at https://marcverhagen.github.io/pages-test/.

Commits on the master branch may be tagged with the site name and a date with so you can revert to prior work.

This site is for experimenting with the MMIF specifications site at https://github.com/clamsproject/mmif. To do that you would copy the contents of the `docs` directory in that site to `docs` in this repository (and probably to `sites` as well if you want to keep track.

To make it work you would have to edit `docs/_config.yml` and change `url` and `baseurl`:

```
url: "https://marcverhagen.github.io"
baseurl: "/pages-test"
```

If you want to experiment with the layout you should also change `remote_theme`:

```
remote_theme: marcverhagen/website-theme
```

Now make changes in https://github.com/marcverhagen/website-theme in the master branch. After that you still need to make a change in `docs` and push it up to see the new theme.

For local testing do the following in the `docs` directory:

```bash
$ bundler exec jekyll serve
```

At the moment this is only good for link testing because my version of Jekyll does not work with remote themes.

*This repository was originally intended for experimenting with a variety of sites, but it is much easier to have a dedicated site each time you want to do some experimentation. So this one will always be for MMIF only.*