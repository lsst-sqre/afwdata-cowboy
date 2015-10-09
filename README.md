afwdata
=======

LSST afw data.


git-lfs
-------

afwdata stores large files using [git-lfs](https://git-lfs.github.com/). LSST runs their own git-lfs and storage services. To use our git-lfs server you need to configure git. Typically through ~/.gitconfig or the repository's .git/config files.

```
[lfs]
	url = "https://git-lfs.lsst.codes"
```

There is **no password required** for cloning or pulling from LSST's git-lfs server or s3 service. But it is recommended that you use a [credential helper](https://help.github.com/articles/caching-your-github-password-in-git/) to avoid being prompted for a username and password repeatedly.

If you are a member of the github lsst organization then you may push using git-lfs. To push you should login using your github username and password to the git-lfs server (git-lfs.lsst.codes).


LICENSE
-------

See the LICENSE file.
