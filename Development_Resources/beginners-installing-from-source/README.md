Reference : http://moi.vonos.net/linux/beginners-installing-from-source/

Copyright © 2021 - Simon Kitching



# Beginner's Guide to Installing from Source

First published on: August 28, 2015

Categories: Linux
## Introduction

This document is intended for users of open-source operating systems who wish to install software direct from the original authors, rather than relying solely on the software (and versions) provided by their operating system. It is written for those who are not familiar with the concept of downloading software in source-code form, providing background information about relevant commands and the process in general.
Concepts Discussed

  * Development and distribution: independent software developers, multi-os support, releases (archives), version-control
  * Distributions: binary packages and package-managers
  * Downloading: http, ftp, wget, checksums and signatures
  * Archive files: tar, zip, gzip
  * Common files: README and INSTALL; required dependencies
  * Patching with sed/awk/patch
  * Building and Installing: configure, make, cmake, perl and python
  * Building and Installing Documentation
  * Compiler settings and stripping; handing errors
  * Post-installation

## Development and Distribution

A typical operating system consists of hundreds of different applications. In a proprietary operating system, the producer/seller of that operating system typically owns and manages the development of all that software. However open-source systems are usually created by obtaining and integrating applications invented and maintained by many independent groups - or even single independent developers. In addition, an open-source software project is often used in a variety of different operating systems - eg Linux-based, BSD-based, Hurd, and sometimes even integrated into proprietary operating systems such as Solaris, Mac, even Windows (if the licence allows).

The original software developers are sometimes referred to by distribution maintainers and end-users as the upstream source or simply upstream. Similarly, the developers often refer to the distributions that use their code, or the end-users as downstream.

Most open-source projects store their source code in a version-control system which is accessible over the internet (read-only for anonymous users). For such projects it is possible to download the very latest “in-progress” files, or to download the set of files “tagged” with some release-id (version number). However it is often not very efficient to do this; projects usually make regular releases by creating an archive file containing all the relevant files and make it available for download. For projects that do not have a public version-control system, such periodically released archive files are the only way to obtain the sourcecode directly.


## Distributions, Binary Packages, and Compiling From Source

There are many operating system distributions which do the work of finding, downloading and tweaking all the most-commonly used software packages. Several also compile it, and make the binary-form results available. There are many benefits, including quicker installation, one location to find relevant software, and particularly a supply of relevant security patches: the distribution maintainers watch for security updates and make it easy for end users to notice and install them.

However such distributions often don’t include the very latest version of software; if you need a newer version than the one provided by your distribution then it may be necessary to build it yourself. Software is also often very customisable at install-time, particularly with the ability to omit features that are not needed. Because a distribution needs to keep a wide range of users happy, they tend to include every feature in the compiled applications they distribute; you as the end-user may be able to tune an application better by compiling it yourself.

Distributions generally include a package manager that keeps a database of which software is installed. It isn’t a good idea to go changing the software on a machine “behind the back” of the package manager; all sorts of odd behaviour could occur later. If your distribution has a package manager, then please read this document for background information - but then consult the documentation for your distribution to find out how to install software without confusing your package manager. Usually this involves writing a package specification that describes the software and then using the local package manager to compile and install the software. This applies to all distributions with package-managers, regardless of whether applications are distributed in binary (pre-compiled) or source-code form.


## Downloading and Security

The usual way to download an archive file is by using a web-browser and clicking on a “download” button, clicking a link, or right-clicking a link and selecting “save as”. This downloads the file using the “http” protocol. Some sites instead make files available via the older “ftp” protocol. Many web-browsers support this too, ie clicking a link can also work here. Alternately, there are ftp client applications.

The “wget” or “curl” command-line application can also be used under unix-like operating systems to fetch a file via http or ftp when the correct URL is known.

Sites which publish software that is very frequently downloaded often have “mirror” sites set up, ie helpful people keep copies of the files in various places around the world. The original site usually has a list of the available mirrors, and you should choose one that is near to you. This helps reduce the cost of network bandwidth on the original publisher, and usually also lets you download faster.

Both the “http” and “ftp” network protocols can be intercepted by criminals or other undesirable parties who can then modify data as it downloads. Data can also potentially be corrupted by accident while underway (though this is not common). And when using a mirror-site, it is possible that someone has modified the files there (ie that the files on the mirror are not the same as those from the original publisher). It is therefore a good idea to verify that what you downloaded is what the original publisher intended.

Many sites provide an md5sum file for each archive file, which holds a checksum of the contents of the file; sometimes a single md5sums file holds checksums for a number of other files. You should always obtain an md5sums file from the original site, never a mirror. And you should download it via the secure https protocol if possible. The unix md5sum commandline tool can then be used to compute the checksum of the big archive file, and compare it to the expected values to ensure the contents are as expected.

To compute the sum of a single file:

```
   md5sum file-to-check
```

and “by hand” verify the output of this application against the expected value. If the value is in a webpage, you can open the “find” dialog on that page and copy-and-paste the value output by the md5sum program. The “find” will match only if the values are the same.

If the software provider provides an md5sums file which has a list of (filename, checksum) pairs, then you can run:

```
   md5sum -c md5sums-file
```

which will look in your local system for every file listed in the md5sums-file, compute its checksum, and report an error if it is not the expected value.

Some software providers sign archive files instead of (or as well as) providing an md5 checksum. In this case you should:

  * download the provider’s public key from their website (using https where possible)
  * download the “signature file” for the archive-file; this will be a small file which has the same base name as the downloaded file, with suffix “.sig” or “.asc”
  * perform the following steps

```
# needed only once for each key, ie each "publisher"
gpg --import {public-key}

gpg --verify {signature-file-name}

The verify step decrypts the signature-file, revealing a checksum; it then runs a checksum algorithm over the real file and checks that they are the same. Obviously, the “gpg” application needs to be installed locally.
```


## Archive Files

An archive is a single file that contains within it a number of other files. There are several different tools for creating such files but in all cases the process is effectively to append all the individual files together, and then add an “index” which contains the offset, length, name and other properties of the original files so that they can be extracted again.

Note: the word “archive” in English can imply something “old”, no longer used, or a “backup” copy. While archive files can be used to store backups or rarely used data, they are also convenient for passing data around a network.

The “tar” application packs multiple files into a single “tar-format” archive file, which is the most commonly-used format in open-source. Tar originally meant “tape archive”, but the format works well on disks too. Tar archives remember not only the original names of files, but also their original Unix “owner id” and file-permissions. The ownerid is seldom useful (unless the tar archive was created on the same machine it is being unpacked on), but the file-permissions are. By convention, tar-format files are usually given names ending in “.tar”. Tar-format files containing sourcecode are sometimes referred to as “tarballs”.

The tar application doesn’t compress the file contents. However source-code files do compress very well and network bandwidth is always too slow and too expensive, so tar files are usually compressed after creation, using a generic compression application. The most commonly used compression type is “gzip”, and the resulting file is usually given the suffix “.tar.gz” or “.tgz”. Compression with bzip2 is also common, and such files are usually given the suffix “.tar.bz2”. Occasionally “xz” compression will be used; files are usually given the suffix “.tar.xz”.

The original version of the tar application was created a long time ago, and it has been reimplemented a number of times. Sadly this means that the commandline options available vary considerably depending on which version of the application you are using. The functionality also varies depending on version; in particular some versions can auto-detect when compression has been used, and decompress automatically while others require the correct commandline parameters to be passed in order to handle compressed files, and yet others require the file to be decompressed first. Here are some example commands to extract files from a tar archive:

```
   # Modern GNU tar options. This works for files compressed
   # with gzip and bzip too
   tar --extract --file filename

   # Same as above
   tar -xf filename

   # Same as above. Leading "-" is optional
   tar xf filename

   # explicitly decompress gzip2-compressed file then
   # pass uncompressed result directly into tar
   gzip -cd filename.tgz | tar xf -

   # same as above, but for bzip2-compressed files
   bunzip2 -cd filename.tar.bz2 | tar xf -
```

Note that if the “f” is omitted, tar just appears to hang (waits for user input).

Warning: unpacking a tar file can overwrite local files. By default, files are unpacked into a subdirectory of the current directory, which should be safe as long as your current directory is something appropriate. However do not trust any instructions that use the following options; they may be trying to trick you into modifying important local files:

```
  -C or --directory
  -P or --absolute-names
  --transform or --xform
```

Most tar-files are created such that unpacking them creates a single subdirectory within the current directory, and all other files are placed into that directory; eg unpacking a file named “foo-1.2.tar.gz” would create a subdirectory named “foo-1.2” with files inside that directory. Sadly not everybody that packages source-code for download follows this convention; sometimes the tarfile expands its contents directly into the current directory - which can create a big mess if that directory already has files in it. It is therefore best to check the contents of the tarfile before unpacking, using the following command:

```
   # Modern GNU tar
   tar --list --file filename

   # Same as above
   tar -tf filename

   # Same as above. Leading "-" is optional
   tar tf filename

   gzip -cd filename | tar tf -
   bunzip -cd filename | tar tf -
```

Occasionally, archive files are distributed in “zip format”. Zip-archives are most common in the DOS and Windows world, or in relation to Java, but are occasionally encountered elsewhere. The Zip format works like a combination of tar and gzip (it uses the same compression as gzip but its own kind of internal “indexing”). Zipfiles do not preserve the original unix ownerid or file-permissions. The contents of such a file can be extracted with the unzip command (assuming it is installed locally).

Where possible, archive files should be unpacked when logged in as a normal user, not the “root” user. This is an extra safety-measure to prevent any unintended file overwrites. However the file-owner settings recorded in the tar-file are only preserved when the user unpacking the archive is the root user. If these are important (which is not common) then the archive must be unpacked “as root”.

## Common Files

Unpacked source-code archives usually contain a file named README or INSTALL (or both) in the top-level directory. You should always read these documents first, as they give important information about how to compile, install and configure the rest of the source-code in the downloaded archive.

One important piece of information usually found in the README or INSTALL is a list of other software that must be installed first. Any program you download will require some local header-files, library-files and/or helper tools to build or to run. If you don’t get the prerequisites right, then the application may not compile, or may compile but not run, or may get built without certain optional features that you want.

Another important piece of information is the set of parameters that can be passed to the build-process; see later.

## Patching

Sometimes the downloaded software is known not to work in your environment, and somebody has already figured out how to tweak it to resolve the problem. The person who solved the problem may publish their “tweak” in the form of a sed or awk command, a shell-script containing multiple sed/awk commands, or a patch file. Obviously, you need to be cautious about such changes, applying them only if you trust the source or have the ability to double-check the changes.

The sed tool applies a regular-expression to each line in a textfile, and replaces matching text with something else. It’s a fairly limited tool, but easy to use and widely available.

awk does something similar, but is capable of performing more complex transformations of textfiles.

A patchfile is created by using the “diff” tool to compare two versions of the same file and output the differences. The patch tool can take the output of “diff” and apply it to one of the files to “convert it” to the other version. The nice thing about patchfiles (ie the output of diff) is that it is quite human-readable, ie it is reasonably easy to see what changes will be made.

## Build Systems: configure, make, cmake, etc

The software developers who created the software you just downloaded obviously need some way of compiling and installing that software on their own machines. Whatever config files are necessary for the tools they use are almost always included in the archive file. As open-source developers want as many people as possible to use their software, they also go to some effort to make it easy to build and install the software on a range of different systems. However they cannot support every possible configuration in the world.

In the end, the point of the installation process is to convert the original source-code into a form that the local computer can execute, and then to place all the necessary files into directories that are listed in the $PATH variable for all users (so they can execute those files). Installing modules for interpreted languages is slightly different; those files get installed where the interpreter (eg python or perl) can find them, rather than in $PATH directly.

### Configure and Make

The most widely-spread tool used to manage the compilation and installation of source-code is make. Make is an application which takes a configuration-file (called a makefile) that contains a list of rules, most of the form:

  * when TARGET-FILE is older than SOURCE-FILE then SOME-ACTION

The target-file is the end product, or some intermediate stage. The source-file is the hand-written source-code, or some intermediate artifact. The action is usually the invocation of a compiler, a linker, or similar which recreates the target-file. This document is far too short to go into the details of the very complex and powerful make command; fortunately it is usually not necessary to understand makefiles to compile software - unless something goes wrong. A brief explanation of makefile syntax and behavior can be found in Appendix A.

Unfortunately, although makefile syntax is very powerful it still isn’t enough to be able to handle all the possible ways that computers can be configured, and all the possible ways that the person installing the software may wish to compile the application. Many software packages therefore come with a shell-script named “configure” and a template makefile named “Makefile.in”. The configure script takes a list of configuration options on the commandline, and converts the template makefile into a real makefile customised for the local computer and the installer’s wishes. The installation sequence therefore usually goes like:

```
# unpack and read documentation
tar xf filename
cd {directory created by above step}
less README
less INSTALL

# generate customised makefile
./configure {some options ...}

# compile everything in the local directory
make

# update global directories
sudo make install
```

By the way: the “configure” script is auto-generated by software called autotools, but that doesn’t matter to the person using it.

Configure is usually invoked as “./configure” to avoid two possible problems:

  * Some users don’t have “.” in their $PATH variable. In particular, the root user doesn’t have this for security reasons
  * Some users don’t have “.” as the first entry in their $PATH, meaning that the wrong configuration script might get run

In general, it is best to perform all steps except “make install” as a normal system user, not root. This avoids mistakes and possibly some attacks (though as the install step is done as root that isn’t much protection). However installing software into the global /bin or /usr directories usually requires administration privileges (unless you’re using a “user-based package manager” or similar rare setup).

Some projects provide a makefile but no “configure” script; in this case the “configure” step above can be omitted. Either the application is simple enough that it doesn’t need it, or the software developers have built more logic into the hand-written makefile.

Not all systems are set up with “sudo” enabled. In this case, use the following instead:

```
su  # must then enter root password
make install
exit
```

For most software, the configure and make commands can be run in the same directory as the source-code, as shown above. The result is that new files generated during compilation get mixed together with the originals, which is somewhat messy, but the “make clean” command can be used to tidy that up later. However for some software it is necessary to create a temporary directory, change the current-working-directory to that directory and then perform the build-steps there; the project documentation should indicate if this is necessary. Some people consider it better to always build from a temporary directory. An example of building using a separate directory next to the original source-code, which is a common convention:

```
# unpack into a directory {packagename}
tar xf filename

# create separate build directory
mkdir {packagename}-build

# compile everything in the separate build directory
cd {packagename}-build
../{packagename}/configure {some options}
make

# update global directories
sudo make install
```

## Other Build Tools

Some projects use cmake as their build-tool. cmake works somewhat like configure (see above); it generates a makefile whose content depends on the options passed to the cmake command, and on features of the local system. The steps require to build a cmake-based package are identical to the “configure/make” examples above except that the configure step is replaced by:

```
cmake . -DCMAKE_BUILD_TYPE=Release {some options ...}
```

As always, check the project’s documentation for instructions on how to build.

Some projects use build-tools based on python or perl rather than make. The principles are still fairly similar.

Software which does not need to be compiled usually has a fairly simple and quick installation process. In particular, applications written in the Perl or Python interpreted languages can be installed just by copying the files into the relevant location. These projects nevertheless include a program or script in the archive-file which performs this task, rather that requiring the installer to do this manually.

## Environment Variables

Options to configure the compilation and installation of an application are usually passed as command-line parameters to the “configure” script or the make program. However sometimes configuration options are passed via environment variables instead. These can be specified by placing the definitions on the start of the command, eg

```
NAME=tom ENABLE_FOO=no ./configure
```

Environment variables can also be defined before running the command:

```
export NAME=tom
export ENABLE_FOO=no
./configure
```

Which options are available is normally described in the archive’s README or INSTALL files, or on the project website. Sometimes the available options can be seen by running ./configure --help.

## Building and Installing Documentation

Some projects provide documentation which can be “installed” so it is accessible via normal system documentation viewers such as “man” or “info”. Some provide documentation in HTML form, which usually gets installed under /usr/share/doc. Sometimes this documentation is included in the “standard” archive file, and sometimes it is a separate (optional) download. Sometimes the documentation is installed as part of the standard make install command, and sometimes a separate command must be used if you wish to install it. And sometimes the documentation is delivered in a “ready-to-use” form, but sometimes it is delivered in a kind of “raw form” that must be processed before being installed - rather like source-code needs to be compiled.

As should be clear by now, the variety of approaches to delivering documentation is so wide that no really useful advice can be given here. See the README and INSTALL files in the downloaded archive, and the project website for guidance.

## Other Build Targets

As well as commands to compile everything (“make”) and to install the previously-compiled programs (“make install”) or documentation, there are a few other common possibilities.

make clean usually removes all generated files, ie leaves the directory as it was after the files were unpacked from the archive.

## Invoking a Compiler

As noted above, the most common step performed by “make” or “cmake” is to invoke a compiler. The local system must have the appropriate compilers installed.

This is also the step that is most likely to fail (along with linking).

If the compilation step fails with an error-message about not being able to find a header-file, or not being able to find a library-file then you have probably not installed all of the pre-requisites - reread the README and INSTALL files. In some cases, the missing prerequisite is optional, in which case there will be a parameter that can be passed to configure or an environment variable which can be set to allow the software to be installed without that prerequisite. Double-check the parameters you specified, and if they seem correct then the project documentation is the best resource for resolving such issues.

Compilers have a range of options that can potentially improve performance. However you should only mess with these if you have plenty of experience. If you need this document, then just leave compiler options at their defaults!

The output of compiling and linking (the “executables” that you actually wanted) usually have significant amounts of data in them which are useful for debugging the programs, but not useful for “normal end users”. This information can be removed from the executable files by running strip {filename} on them. Smaller programs will save disk-space and also load slightly faster. Unless you are intending to debug the program, using strip is a good idea.

## Post-Installation Configuration

Some applications can have their behaviour customised via configuration files read on application startup. Often applications install default versions of the configuration files somewhere under /usr or in the /etc directory. Inspect the output of the make install command to see which config files have been installed. Configuration options should also be documented in the program’s README or INSTALL, or on their website.

## Appendix A: An example Makefile

Unfortunately, when building packages from source-code, it is not unusual for compilation errors to occur. It is sometimes possible to diagnose and fix the problem by inspecting the makefile, ie a basic understanding of makefile syntax can be helpful. Here is a very brief example of the basic syntax and functionality; for further details see the make documentation or one of the many tutorials available online.

A sample makefile to build an executable called ‘prog’ which has one ‘c’ sourcefile, one headerfile and uses one library (which it also builds from a single ‘c’ sourcefile) could look like the following:

```
prog: prog.c prog.h libmylib.a
  gcc -o prog prog.c -L. -lmylib

libmylib.a: libmylib.o
  ar -rcs libmylib.a libmylib.o

libmylib.o: libmylib.c libmylib.h
  gcc -c -o libmylib.o libmylib.c
```

The form of the entries (rules) are:

```
target: dependency1 [dependency-n ...]
<tab> command to execute
...
```

For each “rule”, if the target is missing or older than any of the dependencies (based on file timestamps), then the command(s) are run to (re)create the target. However each dependency is first tested to see if there is a rule that has it as a target. If so, that target is recursively evaluated, ie (re-)built if it is missing or older than its dependencies.

Thus in the above set of rules, a change in libmylib.c will cause libmylib.o to be rebuilt. Then libmylib.a is regenerated and finally prog is rebuilt.

Makefiles can get very complicated and many are automatically generated, but the above principles always apply.

## Acknowledgements

This document was inspired by the TLDP document Software Building HOWTO which sadly is not actively maintained.

Thanks to the following people who gave feedback on this document: Bruce Dubbs, Daniel Schepler.


---------------------

Edited by @TadavomnisT for a ReadMe format.
