# Notice
I made a fork of this because upstream has abandoned it. https://github.com/GitbookIO/gitbook#%EF%B8%8F-deprecation-warning I'll try to keep it working, but I have no idea what I'm doing.

# gitbook-cli

> The GitBook command line interface.

Install this globally and you'll have access to the gitbook command anywhere on your system.

```
$ npm install -g gitbook-cli
```

**Note:** The purpose of the gitbook command is to load and run the version of GitBook you have specified in your book (or the latest one), irrespective of its version. The GitBook CLI only support versions `>=2.0.0` of GitBook.

`gitbook-cli` store GitBook's versions into `~/.gitbook`, you can set the `GITBOOK_DIR` environment variable to use another directory.

## How to install it?

```
$ npm install -g gitbook-cli
```

## How to use it?

### Run GitBook

Run command `gitbook build`, `gitbook serve` (read [GitBook documentation](https://github.com/GitbookIO/gitbook/blob/master/docs/setup.md) for details).

List all available commands using:
```
$ gitbook help
```

#### Specify a specific version

By default, GitBook CLI will read the gitbook version to use from the book configuration, but you can force a specific version using `--gitbook` option:

```
$ gitbook build ./mybook --gitbook=2.0.1
```

and list available commands in this version using:

```
$ gitbook help --gitbook=2.0.1
```

#### Manage versions

List installed versions:

```
$ gitbook ls
```

List available versions on NPM:

```
$ gitbook ls-remote
```

Install a specific version:

```
$ gitbook fetch 2.1.0

# or a pre-release

$ gitbook fetch beta
```

Update to the latest version

```
$ gitbook update
```

Uninstall a specific version

```
$ gitbook uninstall 2.0.1
```

Use a local folder as a GitBook version (for developement)

```
$ gitbook alias ./mygitbook latest
```

