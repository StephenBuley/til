# CD back to previous folder

I am frequently annoyed with being in the wrong place in my folder structure in the command line, but now I can be a little less annoyed. There are all kinds of tricks and this is another one for the tool belt.

```bash
starting/folder > cd my/deeply/nested/folder # travel down into a nested folder
starting/folder/my/deeply/nested/folder > cd - # travel back to the previous directory
starting/folder > # and now I'm back!
```

This has prevented me from having to do `cd ../ cd ../ cd ../` and feels better then `cd ../../../../` and works when you travel up and down the folder structure as well.
