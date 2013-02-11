Xcode-Tips
==========

Some Xcode tips & tricks that I find *kinda* useful...

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

![Hide Debugger When Exists Unexpectedly](Hide%20Debugger%20When%20Exists%20Unexpectedly.png "Hide Debugger When Exists Unexpectedly")
