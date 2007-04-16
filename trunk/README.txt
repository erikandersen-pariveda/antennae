################################################################
# Copyright (c) 2007 Allurent, Inc.
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
It includes the source for arc-flexunit2, the light-weight way
to run FlexUnit tests from the command line, along with the
source that makes up the end-user Antennae distribution.

It is designed to allow testing everything under the Antennae
directory as if a user had just unpacked it. To get it into
this state run "ant stage" from the root directory. This will
copy into Antennae all of the files that make up the distribution
along with your local build-user.properties file, which should
be setup in order to build arc-flexunit2. Once completed cd in
the Antennae directory and test out the samples.
