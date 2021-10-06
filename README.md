# GAUSS
The Generic Animation Unicode Scripting Software (GAUSS) is a set of bindings for an interactive shell designed to simplify and streamline the process of drawing simple graphics using the native functions in an interactive shell. It is useful for drawing in a CLI environment as well as for graphics used by command line programmes. GAUSS was built and tested in a BASH environment on macOS, however it should be compatible with most other Bourne-compatible shells as well as most Linux distributions and Unix flavours (i.e. FreeBSD). The current release is macOS specific so it will have to be installed manually on other systems by appending the contents of *gauss.bindings* to your shell profile (i.e. `FOO=$(cat gauss.bindings); echo "$FOO" >> .bash_profile`).

NOTICE: The most recent build of GAUSS (1.0.1-macOS) has changed the syntax so that all commands with the exception of `$DRAW` and `$ENDDRAW` (now `$endDraw`) are now corporal (lowercase). The installer binary has been uploaded and the files in the code section of the repository have been updated, however any scripts created with the previous release will not work with this one, and they will have to be updated. This only applies to command based scripts, frames saved to a file as raw do not need to be modified to work.

See the Wiki for more info [[https://github.com/tiaghun/GAUSS/wiki]

**NOTICE:** A new version of the GAUSS bindings has been uploaded. This version shebangs `zsh` rather than `bash`, and has been adjusted to be compatible on all UNIX variants (This includes but is not limited to: Linux, BSD, Android [Termux], macOS, Solaris, and System V/Indiana [OmniOS, Tribblix, OpenIndiana]
The only requirement for v2 to work is a copy of Zsh v5.8 installed or symlinked to `/bin/zsh`. For those wanting to use GAUSS to colorize or draw graphics in your shell scripts simply include a `source /path/to/GAUSS` line at the top and include a copy of the GAUSS file with your script. I recommend something like this for good portability:

*In the top of your script, with GAUSS included in the same directory as your script*
`cd "${0%/*}"`
`source ./GAUSS`
`rest of script here`
