# Automatic Generator of New Version and Changelog File
It Increments the current version and updates the changelog file from the commits.

## Artifacts
* **autoVerLog.sh** - The script that does the job;
* **VERSION.txt** - Text file with the current version;
* **CHANGELOG.md** - File with change information.

## Git
This script works with git version control:
* Put tags(number of version) in commits without tags;
* Get the log of commits;
* Commit these changes and push to the master.

## Commit
All commits must to be created from this text syntax: **"type: message (#task)"**
* where:
   * **type** = Commit types: **"new"**(New Features), **"chg"**(Changed Features) and **"fix"**(Bug Fixes).
                Pay attention: the beginning of the text needs to be the type, the colon and a
                space (i.g: **"new: "**);
   * **message** = The message with phrases that may have line breaks and no list definition
                   characters;
   * **task** = Number that represents the commit task.
*   examples:
    * **"new: Allow provided config object to extend other configs. (#73684)"**
    * **"fix: Correct minor typos in code. Update outdated unreleased diff link. (#1783)"**

## VERSIONING
 We suggest the format **X.Y.Z** with more or less numbers (i.g: **1.2**, **1.2.3**, **1.2.3.4**).
 When this script is run, the last number is incremented, for example, the current version is
 **"1.2.3"**, after running this script the new version is **"1.2.4"** and the **VERSION.txt** file is updated.
