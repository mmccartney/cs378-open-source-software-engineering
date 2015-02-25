## Status

I have set up my environment and read through the sample test cases in the documentation.

## Goal

* My current goal is to hopefully figure out why the tests fail when -DskipTests is removed.

* If fixing the broken tests requires more code reveiw, then I will switch to looking through the code some more.

* Another goal is to figure out why my iPhone simulator runs so slow; it may be machine dependent since only Chris and I have this problem.

## Plan

1. Run mvn package (without the -DskipTests)
1. Follow error messages
1. Learn how to use IntelliJ's debugger, it will probably be useful for debugging the tests.
1. Fix tests if it's that simple, otherwise, look over code to figure out what is going wrong.
1. If some tests are fixed, share with Chris, Derek, Thahn, and Josh.
1. Fix the rest of the tests and Pull Request.
