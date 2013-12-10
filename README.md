## Brew Cask Dotfile Generator

If you use [homebrew-cask](https://github.com/phinze/homebrew-cask)
to install applications, you can use a dotfile to keep your apps
consistent across your devices.

See an example [here](https://gist.github.com/seethroughtrees/7902470);

This app will check all of the Applications in your `/Applications`
folder and any Casks you already have installed in your
`/opt/homebrew-cask/Caskroom/`.

Then compare them to a list of current Casks in the homebrew-cask
Github Repo.

Lastly, it will generate a .cask file that is a shell script for
syncing and automating your installs across devices.


### Installation

*this is not implemented yet*

```npm install brew-cask-dotfile```


### Usage

Just type `node app` to generate your script file.

It will generate the .cask file in the current directory.  Move it to
your home directory after to keep it organized.

After you have the file, just run `sh ~/.cask` to run the script!


### Options

##### Set Applications Flag

In homebrew-cask you can have your applications install directly into
the /Applications folder if you want by passing an option.

With brew-cask-dotile you can add the option to your script by adding
the argument `-a` after.

```node app -a```


### Contributing

Feel like making this better?  Great.  Please just add tests to any changes.
You can run the tests with `npm test`.

They're written with [testem](https://github.com/airportyh/testem),
[Mocha](http://visionmedia.github.io/mocha/) and [Chai](http://chaijs.com/).
