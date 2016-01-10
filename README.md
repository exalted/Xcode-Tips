Xcode-Tips
==========

Some Xcode tips & tricks that I find *kinda* useful...

Styling
-------

Make text not be antialiased (useful for non-retina screens) — [makes great sense using Monaco font](https://www.mikeash.com/pyblog/friday-qa-2015-08-14-an-xcode-plugin-for-unsmoothed-text.html). ([Reference](http://stackoverflow.com/a/11675163/11895))

```bash
defaults write com.apple.dt.Xcode NSFontDefaultScreenFontSubstitutionEnabled -bool YES
```

Faster build times by leveraging multi-core CPU
-----------------------------------------------

```bash
defaults write com.apple.dt.Xcode IDEBuildOperationMaxNumberOfConcurrentCompileTasks $(sysctl -n hw.ncpu)
```

Ref.: http://merowing.info/2015/12/little-things-that-can-make-your-life-easier-in-2016/

Disable plugins
---------------

```bash
$ PLUGINS_DIR=/Applications/Xcode.app/Contents/PlugIns
$ f() { local PLUGINS=("IDEGit" "IDESubversion" "IDERepositoryViewer"); for i in ${PLUGINS[@]}; do mv -vni "$PLUGINS_DIR/$i.ideplugin" "$PLUGINS_DIR/$i-disabled.ideplugin"; done }; f; unset -f f;
```

Sweet repos
-----------

* [Xcode-CodeSnippets](https://github.com/exalted/Xcode-CodeSnippets)

Thousand words ;-)
------------------

![Scheme Run Arguments](Scheme%20Run%20Arguments.png "Scheme Run Arguments")

![All Exceptions Break On Throw](All%20Exceptions%20Break%20On%20Throw.png "All Exceptions Break On Throw")

![Exception Breakpoint](http://natashatherobot.com/wp-content/uploads/Screen-Shot-2015-06-30-at-6.28.21-AM.png)

For details for the trick above: http://natashatherobot.com/xcode-debugging-trick/

![Using the power of User Breakpoints](http://merowing.info/2015/12/symbols.png)

For details for the trick above: http://merowing.info/2015/12/little-things-that-can-make-your-life-easier-in-2016/

![Hide Debugger When Exists Unexpectedly](Hide%20Debugger%20When%20Exists%20Unexpectedly.png "Hide Debugger When Exists Unexpectedly")
