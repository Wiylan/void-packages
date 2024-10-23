# A custom XBPS source packages collection

This repository contains a custom XBPS source packages collection for the Void Linux distribution.

See [void-linux/void-packages](https://github.com/void-linux/void-packages) for details.

## Table of Contents

- [Packages](#packages)
- [Building](#building)

## Packages

## Building

Clone this git repository:

```
$ git clone --single-branch --branch main https://github.com/Wiylan/void-packages.git custom
```

Clone the `void-linux/void-packages` git repository:

```
$ git clone https://github.com/void-linux/void-packages.git
```

Copy the custom `srcpkgs`:

```
$ cp --recursive custom/srcpkgs void-packages
```

Install the bootstrap packages:

```
$ cd void-packages
$ ./xbps-src binary-bootstrap
```

Build a package:

```
$ ./xbps-src pkg <pkgname>
```

Once built, the package will be available in `hostdir/binpkgs`.
To install the package:

```
# xbps-install --repository hostdir/binpkgs <pkgname>
```

