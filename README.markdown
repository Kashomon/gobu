Gobu: A Go Build Tool
====

![Gobu Test Failure](http://i.imgur.com/uVg9sDa.png)

Gobu is simple [Go](http://www.golang.org) build tool for Vim.

The primary improvement of Gobu over a default quickfix integration is that the
entire output of a command is put into the Gobu Window.  This means that we get
the entire message -- no truncation, no munging, *and* we still get the useful
jump-to-error feature of quickfix (by pressing enter while on the same line as
a file path).

Gobu exposes the following commands to the user:

      :GoBuild -- build current package
      :GoInstall -- install current package
      :GoTest -- test current package
      :GoFmt -- go format current package

Gobu also supports recursive versions of the commands, by adding a trailing
bang:

      :GoBuild! -- recursive build, starting from current package
      :GoTest! -- recursive test, startingc from current package

### The Gobu Window

Right now, the GobuWindow remaps following keys:

      <CR> (enter) -- jump to a file location under the cursor
      R -- rerun the last command
      q -- close the window

### Installing

The easiest way to install is to use Vundle or Pathogen (or another vim plugin
manager manager).  For Vundle, all you need to add to your .vimrc is:

      Bundle 'Kashomon/gobu'

and then do a :BundleUpdate

## Examples:

### Panic!

![Gobu Panic](http://i.imgur.com/5eD6hSl.png)

### Test Failure

![Gobu Test Failure](http://i.imgur.com/f830dJX.png)

