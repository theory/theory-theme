Theory Octopress Theme
======================

This [Octopress] theme is a fork of [Aron Cedercrantz]’s [BlogTheme]. It
builds on the great basics there to add these features:

* [Solarized] code markup
* Type displayed with the open-source Adobe fonts [Source Sans Pro] and
  [Source Code Pro]
* Support for [LinkLog] posts (as implemented by [this pull request])

Installation
------------

The theme is for the [Octopress] blogging system. To install it either
[download the theme](https://github.com/theory/theory-theme/zipball/master)
and drop the directory into the `./.themes` directory, or add this repository
as a submodule:

    git submodule add https://github.com/theory/theory-theme.git .themes/theory-theme
    git submodule update --init

You then need to tell Octopress to "use" the new theme.

    rake 'install[theory-theme]'

Test it out by running `rake generate && rake preview`.

Updating the Theme
------------------

### Git Submodule

    cd .themes/theory-theme
    git pull
    cd ../..
    rake 'update_source[theory-theme]'
    rake 'update_style[theory-theme]'
    
Done, test it with `rake generate && rake preview`.

### Manually Installed  Directory

1. [Download the theme](https://github.com/theory/theory-theme/zipball/master)
   from GitHub.
2. Copy it into your `.themes` directory.
3. Update it:

        rake 'update_source[theory-theme]'
        rake 'update_style[theory-theme]'

Done, test it with `rake generate && rake preview`.

License
-------

This theme is licensed under the "Simplified BSD license" (2-clause). For the
exact terms please see the [`LICENSE` file].

[Octopress]: http://octopress.org/
[Aron Cedercrantz]: http://aron.cedercrantz.com/
[BlogTheme]: https://github.com/rastersize/BlogTheme/
[Solarized]: http://blog.teamtreehouse.com/solarized
[Source Sans Pro]: https://github.com/adobe/source-sans-pro/
[Source Code Pro]: https://github.com/adobe/source-code-pro/
[LinkLog]: http://octopress.org/docs/blogging/linklog/
[this pull request]: https://github.com/imathis/octopress/pull/1320
[`LICENSE` file]: https://github.com/rastersize/BlogTheme/blob/master/LICENSE
