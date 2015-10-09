afwdata
=======

LSST afw data.


git-lfs
-------

afwdata stores large files using [git-lfs](https://git-lfs.github.com/). To use afwdata you must install git-lfs and configure it. LSST runs their own git-lfs server and storage service. Git and git-lfs must configured to use our server.

Add this to your git configuration. Typically `~/.gitconfig` or the repository's `.git/config` file.
```
[lfs]
	url = "https://git-lfs.lsst.codes"
```

There is **no password required** for cloning or pulling from LSST's git-lfs server or s3 service. But it is recommended that you use a [credential helper](https://help.github.com/articles/caching-your-github-password-in-git/) to avoid being prompted for a username and password repeatedly.

If you are a member of the github lsst organization then you may push using git-lfs. To push you should login using your github username and password to the git-lfs server (git-lfs.lsst.codes).


LICENSE
-------

See the LICENSE file.
