# makefile
## ressources
- [powerpoint intro](file:///Users/sbars/Documents/devlog/attachments/Makefile.pdf)
  - set of rules to commpile
  - contains dependency rules (programs/dependencies your program is calling, necessary for it to work)
  - commonly used to build/compile a program correctly
  - I don't think this doc is relevant actually
- [GNU make docs](https://www.gnu.org/software/make/manual/make.html)
  - big doc, I think the first sections will be useful
  - each time you type the make command, your files are recompiled, following the instructions you put in the makefile
    - Makefiles can be timesaving to give compilation instructions that are identical accross dozens of files
  - Instructions on how to read this manual
    - If you are new to make, or are looking for a general introduction, **read the first few sections of each chapter, skipping the later sections.** In each chapter, the first few sections contain introductory or general information and the later sections contain specialized or technical information. The exception is the second chapter, An Introduction to Makefiles, all of which is introductory.
  - How make works
    - `target : prerequesites`
      *tab* `recipe (cli commands)`
    - Targets are read from beginning of page. If an unbuilt file is in the first prerequesites, make will move down and execute the one below, until they're all done
      - >The recompilation must be done if the source file, or any of the header files named as prerequisites, is more recent than the object file, or if the object file does not exist.
    - You can set variables to replace a large number of files by a simple string, preventing errors
      - `variable_name = object1.o object2.o etc.o`
      - above the other things
      - access variable with `$(variable_name)`
      - 