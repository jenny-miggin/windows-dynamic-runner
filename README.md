# windows-dynamic-runner

In this `merge-all-config` branch, config files listed in `.circleci/modular-config-list-main.txt` or `.circleci/modular-config-list-feature.txt` are merged at runtime, depending on the name of the branch. 

Different lists (`modular-config-list-feature` and `modular-config-list-main`) exist for different conditions i.e. `branch`, and then conditional statements are applied at a workflow level