---
layout: post
title:  "Hello World!"
date:   2016-08-10
author: "Zetok Zalbavar"
categories: qTox update website repositories OSX Linux
---


And hello to you, internet citizen, visiting the first post on the qTox blog! :)

# The website

As you might have heard, qTox got a new [website]. You might be wondering why
it would be needed, since there is already the `tox.chat` website?

## Why?

There are several reasons. For a long time the `tox.chat` website served to qTox
users instructions that are simply incorrect, if not outright broken. Affected
are Linux and OSX users.

There are also [issues with the `tox.chat` website itself](#website-issues).

### Linux packages & OSX builds

Linux users were directed to `tox.chat` repository, where they could get only
half-broken qTox packages (lack of system/DE integration, no useful
information for debugging) or were told that their distribution is not
supported.

Properly packaged qTox for variety of distributions has been available for a
long time, and qTox's `README.md` pointed to them.

OSX users were told that there are no OSX builds of qTox.

Well, guess what, there are [OSX builds] available.

### Website issues

qTox aims to be available to as many people as possible. This requires support
for languages other than English, whether it comes to the software itself, or
its website.

The `tox.chat` website does not have any localization. It's really sad when
people who are unfamiliar with English are being neglected.

qTox's [website] supported languages from the start. 48 of them currently, and
thanks to [Weblate], it's easy for everyone to update current translations &
add new ones. Both for the website and software itself :)


# The blog

You might be wondering why a Blog is needed, if there is already one under
`tox.chat`.

Well, this too didn't work. The answer to a query about a post for the new qTox
release was that there's not enough to write to mandate a blog post. :(

So, a qTox Blog was needed :)

There are no artificial limits on posting to the qTox blog – the only
requirements are:

* a bit of knowledge about making a pull request on GitHub
* Markdown formatting
* being related to qTox

To add a post, one needs to just add a file in the [`_posts/`] directory, named
`YYY-MM-DD-Name-of-post.md` in [blog's repository]. For real world examples one
can always look at other posts.

For more information about how to blog, the [Jekyll docs] might come useful.


# Linux repositories

As mentioned earlier, qTox is available on a variety of distributions. This is
possible thanks to [Anton Batanev], who not only [packages Tox clients] on
[OpenSUSE Build Service], but also maintains [`pytoxcore`] – Python bindings to
`toxcore`.

He even made a [PPA] for Ubuntu for `arm64`, `armhf` and `ppc64el`
architectures.

Kudos to him for the awesome work!

## Move to OBS

As mentioned before, packages from `tox.chat` repository didn't work well, or
at all and lots of distributions weren't properly supported.

OBS fixes it all, and adds more. It provides packages for CentOS, Fedora and
OpenSUSE, and makes debug information available as package that one can install.

Even distributions as old as Ubuntu 12.04 can get properly packaged qTox
from it. Or CentOS 6(!).


# OSX builds

A bit of old news by now – thanks to the awesome work of [Joseph Krieger] each
new qTox version will be built on Travis CI & deployed to [releases].


# Repository

## More maintainers

qTox gained 2 new maintainers, [@Diadlo] and [@initramfs] \o/

Pull requests to qTox have been going a bit slowly lately. As you might have
suspected, maintainers didn't have enough free time to review & merge all the
new features & fixes by themselves. Now that the load has been leveled, reviews
& merge should move more swiftly.

What does it mean?

Most likely more often releases of qTox, with more stuff \o/

[One just happened](#qtox-150-release) :D


## The move

As you might have noticed, repository has been moved on GitHub from under
`tux3` to the `qTox` organisation. The change nicely reflects that qTox is not a
"one man project" anymore, but something developed by a vibrant community.


## Branch deprecation

It was decided that the branch `stable` is no longer needed for anything,
and might only mislead people. Thus it enters into a 6-months long period of
deprecation, after which it will be deleted.

If anyone was depending on it for anything, they shouldn't – use git tags
instead. Or the `master` branch.


# qTox 1.5.0 release

*Video fixes, video fixes everywhere!*

And lots of other things. There's a nice [changelog]. And yeah, it is rather
massive, since there were a lot of changes, improvements & fixes in qTox.

For OSX users, there's another special release, [1.5.1], and again, no code
changes from 1.5.0 :)

If you're wondering what other things await in the future, there is a [1.6.0]
milestone planned. It might look small, but it just shows items that new
release will require – aside from them, everything that gets merged in between
releases will be available in 1.6.0.

![cat qTox update](https://i.imgur.com/ytnHj2K.gif)

*Incoming qTox update, faster, better, stronger than ever before ;)*


[1.5.1]: https://github.com/qTox/qTox/releases/tag/v1.5.1
[1.6.0]: https://github.com/qTox/qTox/milestone/4
[Anton Batanev]: https://github.com/abbat
[blog's repository]: https://github.com/qTox/blog
[changelog]: https://github.com/qTox/qTox/blob/v1.5.0/CHANGELOG.md#v150-2016-08-09
[@Diadlo]: https://github.com/Diadlo
[@initramfs]: https://github.com/initramfs
[Jekyll docs]: https://jekyllrb.com/docs/home/
[Joseph Krieger]: https://github.com/RowenStipe
[OpenSUSE Build Service]: https://software.opensuse.org/download.html?project=home%3Aantonbatenev%3Atox&package=qtox
[OSX builds]: #osx-builds
[packages Tox clients]: https://github.com/abbat/tox.pkg
[`_posts/`]: https://github.com/qTox/blog/tree/gh-pages/_posts
[PPA]: https://launchpad.net/%7Eabbat/+archive/ubuntu/tox
[`pytoxcore`]: https://github.com/abbat/pytoxcore
[releases]: https://github.com/qTox/qTox/releases
[Weblate]: https://hosted.weblate.org/projects/tox/website/
[website]: https://qtox.github.io/
