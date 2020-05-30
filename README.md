OpenDocument.test
===

you don't need this. go away!

file name
===

<group>-<comment>-<id>[$<password>$].<type>

group    ... primary issue eq. "style", "exception", ...
             if not defined yet: "undefined"
comment  ... comment for this file
             should also contain an issue number from github
             eq. "issue14", if there is one
             if not defined yet: "undefined"
id       ... just a run number for the previous string
password ... defined if the file is encrypted by itself
type     ... file extension

regex: ^(.*?)-(.*)-([1-9][0-9]*)(?:\\$(.*)\\$)?\\.(f?od[tspbgf])$
