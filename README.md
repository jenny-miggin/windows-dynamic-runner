# windows-dynamic-runner

`selectively-merge-configs`: Combo of path-filtering and merging config files. 

In this example, a list of directories is provided in `list-of-dirs-to-monitor.txt`. 

This lists the directories that are checked for file changes during the setup phase. 

If a file change is detected in, for example, `NotepadTest`, then the list of config files defined within `NotepadTest/.circleci-config-dependencies` are merged at runtime, and sent to the continuation endpoint API i.e. all the applicable workflows within the configs are run.