# Configuration

### Leiningen

CIDER launches a Clojure REPL using your Clojure project's build tool (Leiningen for this tutorial). CIDER provides "middleware" (in the form of a Clojure library) to enhance the standard Clojure REPL with additional functionality. 

The recommended method for configuring CIDER's middleware in Leiningen is in the global ```profiles.clj``` file. The global ```profiles.clj``` specifies Leiningen configuration settings that are available across all your Clojure Leiningen projects. 

On Linux and Mac OS X ```profiles.clj``` resides in the ```~/.lein``` directory. On Windows the directory is typically ```%USERPROFILE%\.lein``` (i.e. ```C:\Users\<username>\.lein```).

**Note:** ```profiles.clj``` does not exist by default so you will need to create the file if it does not exist.
    
Add the following to the global ```profiles.clj``` to inject CIDER's middleware:
    
```
{:repl {:plugins [[cider/cider-nrepl "x.y.z"]]}}
```
    
where ```"x.y.z"``` is the version of the CIDER Emacs package that you installed (e.g. "0.14.0"). 
    
Example:
    
```
{:repl {:plugins [[cider/cider-nrepl "0.14.0"]]}}
```



