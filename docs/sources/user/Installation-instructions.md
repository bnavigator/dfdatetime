# Installation instructions

## pip

**Note that using pip outside virtualenv is not recommended since it ignores
your systems package manager. If you aren't comfortable debugging package
installation issues, this is not the option for you.**

Create and activate a virtualenv:

```bash
virtualenv dfdatetimeenv
cd dfdatetimeenv
source ./bin/activate
```

Upgrade pip and install dfDateTime dependencies:

```bash
pip install --upgrade pip
pip install dfdatetime
```

To deactivate the virtualenv run:

```bash
deactivate
```

## Ubuntu 18.04 and 20.04 LTS

To install dfDateTime from the [GIFT Personal Package Archive (PPA)](https://launchpad.net/~gift):

```bash
sudo add-apt-repository ppa:gift/stable
```

Update and install dfDateTime:

```bash
sudo apt-get update
sudo apt-get install python3-dfdatetime
```

## Windows

The [l2tbinaries](https://github.com/log2timeline/l2tbinaries) contains the
necessary packages for running dfDateTime. l2tbinaries provides the following
branches:

* main; branch intended for the "packaged release" of dfDateTime and dependencies;
* dev; branch intended for the "development release" of dfDateTime;
* testing; branch intended for testing newly created packages.

The l2tdevtools project provides [an update script](https://github.com/log2timeline/l2tdevtools/wiki/Update-script)
to ease the process of keeping the dependencies up to date.

The script requires [pywin32](https://github.com/mhammond/pywin32/releases) and
[Python WMI](https://pypi.org/project/WMI).

To install the release versions of the dependencies run:

```
set PYTHONPATH=.

C:\Python3\python.exe tools\update.py --preset dfdatetime
```
