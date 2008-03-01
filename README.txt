################################################################
# Copyright (c) 2007-2008 Allurent, Inc.
# http://code.google.com/p/antennae/
#
# Permission is hereby granted, free of charge, to any person obtaining
# a copy of this software and associated documentation files (the
# "Software"), to deal in the Software without restriction, including
# without limitation the rights to use, copy, modify, merge, publish,
# distribute, sublicense, and/or sell copies of the Software, and to
# permit persons to whom the Software is furnished to do so, subject to
# the following conditions:
# 
# The above copyright notice and this permission notice shall be
# included in all copies or substantial portions of the Software.
# 
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
# EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
# MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
# NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
# LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
# OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
# WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
################################################################

This is the root of the development source tree for Antennae.
It includes the source for arc-flexunit, the light-weight way
to run FlexUnit tests from the command line, along with the
source that makes up the end-user Antennae distribution.

It is designed to allow testing everything under the Antennae
directory as if a user had just unpacked it. To get it into
this state follow these steps:

    1. Create a build-user.properties file (or copy an
       existing version) in the root directory where
       you found this README.txt file. (See
       [root]\Antennae\*.build-user.properties
       for sample files.)

    2. Open a console (aka command prompt window) and
       use the cd command to switch to the same root
       directory.

    3. Type "ant stage" and hit return.

This will copy all of the files that make up the
distribution into the [root]\Antennae subdirectory.

Once completed you can cd into [root]\Antennae and test
out the samples.

For more details on Antennae, see
[root]\Antennae\README.txt.

For more details on Ant, see
http://ant.apache.org/manual/
    