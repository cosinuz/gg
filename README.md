`gg`
==
[![Build Status](https://travis-ci.org/qw3rtman/gg.svg?branch=master)](https://travis-ci.org/qw3rtman/gg)&nbsp;
![](https://img.shields.io/npm/dm/gitgoodies.svg)&nbsp;
![npm version](http://img.shields.io/npm/v/gitgoodies.svg)&nbsp;
[![npm version](https://badge.fury.io/js/gitgoodies.svg)](http://badge.fury.io/js/gitgoodies)&nbsp;
![](https://img.shields.io/npm/l/express.svg)&nbsp;  
[![NPM](https://nodei.co/npm/gitgoodies.png?mini=true)](https://nodei.co/npm/gitgoodies/)


##The Cookbook of Git Goodies

![status](http://qw3rtman.github.io/gg/screenshots/status.png)
![log](http://qw3rtman.github.io/gg/screenshots/log.png)

`gg` helps you *work with `git` more efficiently*, saving you keystrokes for your most prized projects.

Think of `gg` as a wrapper for the `git` commands that you run all the time.

## Getting Started
After the [super painless installation](#installation), suppose we want to clone the [awesome spark shell script (created by Zach Holman)](https://github.com/holman/spark).
![status](http://qw3rtman.github.io/gg/screenshots/clone.png)
Alright, let's switch into that directory.
![gettingstarted2](http://qw3rtman.github.io/gg/screenshots/gettingstarted2.png)
After making a quick change, let's check the status of our clone.
![gettingstarted3](http://qw3rtman.github.io/gg/screenshots/gettingstarted3.png)
Looks like we haven't staged our changes.

In the standard git workflow, we would have to `git add -A` and then `git commit -m "Updated example in README."`.

With `gg`, we can simply `gg c Updated example in README.` and we're good to go.
![gettingstarted4](http://qw3rtman.github.io/gg/screenshots/gettingstarted4.png)
Let's check our clone's status again.
![gettingstarted5](http://qw3rtman.github.io/gg/screenshots/gettingstarted5.png)
Looking good!

## Installation
`gg` can be installed via the Node Package Manager (`npm`).

```sh
	$ npm install -g gitgoodies
```

If that doesn't work, try running it as root. `$ sudo npm install -g gitgoodies`

You can also get up and running without npm, but it is not recommended to do so.

```sh
	# Clone the repository.
	$ git clone https://github.com/qw3rtman/gg.git

	# Switch into the repository's directory.
	$ cd gg

	# Install!
	$ npm install -g

	# Install as root, if the above command does not work.
	$ sudo npm install -g
```

`gg` relies on Node.js and `git`.

Don't foget to `alias gg='noglob gg'` (alias `gg` to `noglob gg`) if you're using [prezto](https://github.com/sorin-ionescu/prezto), [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh), or something similar.

As the standard git plugin for [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) already has uses `gg` as an alias for `git gui citool`, I recommend either unaliasing the [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) plugin alias if you don't use it by placing `unalias gg` at the end of `~/.oh-my-zsh/plugins/git/git.plugin.zsh`, or aliasing `gg` with a different alias, such as `ggg`.

## Updating
Changes are published to the [npm package](https://www.npmjs.com/package/gitgoodies), which is kept up-to-date with this GitHub repository. Simply update via npm:

```sh
	# Update gg
	$ npm update -g gitgoodies
```

## FAQ
### Hold up. Aren't these basically Git aliases?
There's more to the package than just shortcuts or aliases.

For example, the `gg s` command presents you with an easy to look at a quick glance status of your repository. In addition, there are aesthetic changes that increase the intuitiveness of Git itself.

Here's a screenshot of the `gg s` command in action:

![`gg s`](http://i.imgur.com/qXSPuv4.jpg)

### Why Node?
There's nothing special in Node that caused me to select it for this project. I wanted to get my feet wet with a new language and was recommended to try Node.

As Node is fairly popular (from what I've seen), I didn't think the issue of an extra dependency would exist.

In addition, I felt Node would widen the audience that could both understand and contribute to `gg`, compared to Bash.

Also, Node is platform-agnostic, unlike Bash, which is only happy on Unix-based systems.

### How do I get my shell to look like the screenshots?
I'm using the [zsh shell](http://www.zsh.org/) with the miloshadzic [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) theme.

If you are having issues with how `gg` looks and not the shell itself, please submit an issue and we'll attempt to solve the problem.

## Usage
### Initializing repositories
![initialize](http://qw3rtman.github.io/gg/screenshots/initialize.png)
* `gg i`
* `gg init`
* `gg initialize`

### Generating .gitignores
![gitignore](http://qw3rtman.github.io/gg/screenshots/gitignore.png)
* `gg ig`
* `gg ignore`
* `gg ig java`
* `gg ignore java`

### Cloning repositories
![clone](http://qw3rtman.github.io/gg/screenshots/clone.png)
* `gg cl https://github.com/holman/spark.git`
* `gg clone https://github.com/holman/spark.git`
* `gg cl git@github.com:holman/spark.git`
* `gg clone git@github.com:holman/spark.git`
* `gg cl holman/spark`
* `gg clone holman/spark`

### Adding changes
![add](http://qw3rtman.github.io/gg/screenshots/add.png)
Specify which files to add.
* `gg a`
* `gg add`

Add all files.
* `gg aa`

### Committing changes
![commit](http://qw3rtman.github.io/gg/screenshots/commit.png)
* `gg c`
* `gg ci`
* `gg commit`

### Pushing commits
![push](http://qw3rtman.github.io/gg/screenshots/push.png)
* `gg p`
* `gg push`

### Pulling commits
![pull](http://qw3rtman.github.io/gg/screenshots/pull.png)
* `gg pl`
* `gg pull`

### Fetching commits
![fetch](http://qw3rtman.github.io/gg/screenshots/fetch.png)
* `gg f`
* `gg fetch`

Fetch all (`git fetch -all`)
* `gg fa`

### Viewing status
![status](http://qw3rtman.github.io/gg/screenshots/status.png)
* `gg s`
* `gg st`
* `gg status`

### Viewing log
![log](http://qw3rtman.github.io/gg/screenshots/log.png)
* `gg l`
* `gg log`

### Creating branches
![branch](http://qw3rtman.github.io/gg/screenshots/branch.png)
* `gg b`
* `gg branch`
* `gg b new-branch`
* `gg branch new-branch`

### Checking out branches
![checkout](http://qw3rtman.github.io/gg/screenshots/checkout.png)
* `gg ch`
* `gg checkout`
* `gg ch new-branch`
* `gg checkout new-branch`

## Contributing
Contributions are always welcome.

We follow [Airbnb's coding standard](https://github.com/airbnb/javascript), so make sure you use that as a guideline.

Fork our code, make a new branch, and send a pull request.

TODO:
* handling for merge conflicts
* support for specifying path of repository initialization and cloning
* unit tests
* [custom routines](https://github.com/qw3rtman/gg/issues/5)
* check if directory is an existing Git repository or not
* proper colors, regardless of terminal colors/themes
* add verbose option (`gg pl v`, etc.)
* **switch over to [libgit2](https://libgit2.github.com)**
* undo last commit
* add custom files/directories to .gitignore
