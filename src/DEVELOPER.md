Folders
=======

Purpose of each folder:

utils
  General purpose definitions and routines

config
  Files generated by configure script

ocaml
  Selected ocaml parser & typer, as a symbolic link to:
    ocaml_400
    ocaml_401
    ocaml_402

ocaml_aux
  Auxiliary definitions shared by all ocaml versions

kernel
  Wrap ocaml frontend into an incremental parser and typer, with error
  recovery, encapsulate various side-effects of the frontend, etc.
  All access should be done through the Merlin_lib module.

analysis
  Reuse kernel state to:
  - provide completions,
  - locate definitions,
  - type fragments of a file,
  - ...

frontend
  Main entry point to Ocamlmerlin binary, providing commandline interface,
  communication with editors, etc.