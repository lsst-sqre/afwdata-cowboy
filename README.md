afwdata
=======

Test data used to exercise the LSST Stack, including the afw package.


git-lfs
-------

afwdata stores large files using [git-lfs](https://git-lfs.github.com/). To use afwdata you must install git-lfs and configure it. LSST runs its own git-lfs server and storage service. Git and git-lfs must be configured to use our server.

Add this to your git configuration, typically in `~/.gitconfig` or the repository's `.git/config` file.
```
[lfs]
	url = "https://git-lfs.lsst.codes"
```

There is **no password required** for cloning or pulling from LSST's git-lfs server, but it is recommended that you use a [credential helper](https://help.github.com/articles/caching-your-github-password-in-git/) to avoid being prompted for a username and password repeatedly.

If you are a member of the lsst GitHub organization, then you may push using git-lfs. To push, you should login using your GitHub username and password to the git-lfs server (git-lfs.lsst.codes).


Setup
-----

### Mac OS X

```bash
brew install git-lfs
git config --global credential.helper osxkeychain # A credential helper is highly recommended.
git lfs init
git config --global lfs.url 'https://git-lfs.lsst.codes'
git clone ...
```

This will install git-lfs, initialize it, configure the osxkeychain credential helper and configure the LSST git-lfs server.

```bash
Username for 'https://git-lfs.lsst.codes': <GitHub Username OR Blank>
Password for 'https://<git>@git-lfs.lsst.codes': <GitHub password OR Blank>
```

If you are only interested in cloning or pulling, username and password may be left blank.

If you are a member of the lsst GitHub organization, then you can use your GitHub username and password to push to the git-lfs server.

```bash
Username for 'https://s3.lsst.codes': <Empty>
Password for 'https://s3.lsst.codes': <Empty>
```

There is no username or password for LSST's S3 service.


### Linux

[Download and install](https://github.com/github/git-lfs/releases/tag/v1.0.0) the current git-lfs.

```bash
git config --global credential.helper cache # A credential helper is highly recommended.
git lfs init
git config --global lfs.url 'https://git-lfs.lsst.codes'
git clone ...
```

This will initialize git-lfs, configure the cache credential helper, and configure the LSST git-lfs server.

```bash
Username for 'https://git-lfs.lsst.codes': <GitHub Username OR Blank>
Password for 'https://<git>@git-lfs.lsst.codes': <GitHub password OR Blank>
```

If you are only interested in cloning or pulling, username and password may be left blank.

If you are a member of the LSST GitHub organization, then you can use your GitHub username and password to push to the git-lfs server.

```bash
Username for 'https://s3.lsst.codes': <Empty>
Password for 'https://s3.lsst.codes': <Empty>
```

There is no username or password for LSST's S3 service.


Credential Helpers
------------------

GitHub has excellent documentation on configuring [credential helpers](https://help.github.com/articles/caching-your-github-password-in-git/).

If you do not use a credential helper, git-lfs will repeatedly ask for your username and password. This can be very frustrating. To avoid globally installing a credential helper, use git's cache credential helper. By default, it will work for 15 minutes before expiring.

```
git config --global credential.helper cache
```

If your home directory is on a network filesystem, you may need to specify a local filesystem for the cache's socket: "`git config --global credential.helper 'cache --socket /path/to/local/dir/.git-credential-socket'`"

LICENSE
-------

See the LICENSE file.
