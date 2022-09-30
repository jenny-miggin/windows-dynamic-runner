# windows-dynamic-runner

There are 3 branches here.

* Main: just a basic implementation of the path filtering orb

* merge-all-config: Config files listed in `.circleci/modular-config-list-main.txt` or `.circleci/modular-config-list-feature.txt` are merged at runtime, depending on the name of the branch. 

* selectively-merge-configs: Combo of path-filtering and merging config files. In this example, a list of directories is provided in `list-of-dirs-to-monitor.txt`. This lists the directories that are checked for file changes during the setup phase. If a file change is detected in, for example, `NotepadTest`, then the list of config files defined within `NotepadTest/.circleci-config-dependencies` are merged at runtime, and sent to the continuation endpoint API i.e. all the applicable workflows within the configs are run. 