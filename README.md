picam-native
============

This project is the native native library counterpart to [picam](https://github.com/caprica/picam).

Previous versions of picam used JNA, the latest versions use a pure JNI solution as provided by
this project.

The implementation is based on the original source code for Raspistill, but with a significant
re-write. See README.BROADCOM for the original copyright notice.

Building the shared library
---------------------------

Clone the source to a directory on your Pi.

Execute the "pi.sh" command to produce a "picam.so" shared library that your Java picam application
can then use.

However, there is no real need to build the library yourself - a pre-built version is bundled with
the picam-2.x distribution jar and this can be automatically extracted and loaded.

TODO
----

 - TODO think about using vcos_log_error
 - TODO any remaining configuration values to set from the Java (or that were missing generally)
 - organise this native project a bit more (makefile?)
 - issue of sometimes the capture not completing (mmal_server error in logs, same as picam issue?)
 