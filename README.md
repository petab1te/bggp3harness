bggp3 entry
==============

This was our first time fuzzing, I'm pretty sure we found an actual bug in the file sadtrombone.fuzz but then it got patched and we couldn't reproduce it. Lesson learned about using libraries shipped on the target without making backups.
Then we started fuzzing this example and we got some errors, we think the error is probably in our code, but it's crashing in the library, so we figured it would be more fun to just start shrinking it. To do this fast and because we are noobs, we made an extremely dumb fuzzer that shrinks the file by blindly guessing groups of bytes and testing if the crash is still possible. We got it down to 166 bytes which isn't crazy or anything but is decently small for a jpeg. This was pretty fun and we both liked fuzzing immediately, we will definitely be doing it more in the future.
