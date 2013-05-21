MCLIDE
======

Macintosh IDE for Clojure and other Lisp-related languages.

  https://mclide.com

A prebuilt version of MCLIDE can be downloaded from the link above.

== Build ==

MCLIDE 2.x runs on 64 bit OSX 10.6 and later.

Preliminary instructions to get started:

  1. Open a Terminal and change directory to here.

  2. Download MCLIDE 2:

     $ curl -C - -O https://mclide.googlecode.com/files/MCLIDE-20a0-b95dbee-.dmg

  3. Open the .dmg and find the MCLIDE application.

  4. Show the package by control-clicking on the application icon

  5. Locate the following directories in the application and copy them here:

  * Contents/Resources/lib/

  * Contents/resources/slime-2012-02-02/

  6. Rename 'slime-2012-02-02' to 'slime'

  7. Download Clozure CL 1.7 and place its 'ccl' directory here:

     $ curl -O ftp://ftp.clozure.com/pub/release/1.7/ccl-1.7-darwinx86.tar.gz

  8. Execute in the Terminal to build MCLIDE:

     $ sh ./build.sh


== Usage ==

  See instructions in the README file in the MCLIDE build for instructions on how to connect MCLIDE with a development environment or runtime.

== Using with Clojure ==

You can use Leiningen to start clojure with swank then connect from MCLIDE.

If you use Leiningen 2 then add the following to the project.clj file:

    :plugins [[lein-swank "1.4.5"]]

Execute this on the command line to start swank, then after a brief moment connect to port 4005 from MCLIDE:

    lein swank


