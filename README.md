# Bad Password Hashes

A list of over 320,000,000 SHA-1 hashes from hacked password lists. This list is provided by [Troy Hunt](https://www.troyhunt.com/introducing-306-million-freely-downloadable-pwned-passwords/), curator of the website [Have I been pwned?](https://haveibeenpwned.com/Passwords).

There are no changes from Troy's list, other than merging his multiple files together into a single list. I am providing this via Git because it may be more useful to fetch them over Git, including the automatic resolution of deltas in case Troy posts a new update file.

**THIS IS A VERY BIG LIST.** It is around 12 GB, uncompressed.

## See Also…

> **NOTE:** This is a list of known-bad password SHA-1 hashes. For a list of known-bad clear text passwords, see https://github.com/skyzyx/bad-passwords.

## Merging Troy's Lists Manually

These files are large enough that they will crash pretty much any text editor out there. So we will rely on shell tools instead which can handle streams.

## Notes for later improvements

```
LC_ALL=C sort --parallel="$(nproc --all)" -u input > output
```

* http://sgolconda.blogspot.com/2015/11/sort-very-large-dataset.html
* https://unix.stackexchange.com/questions/3770/how-to-merge-all-text-files-in-a-directory-into-one

Needs modern enough GNU sort (post-2010). macOS’ BSD sort will not likely work.
