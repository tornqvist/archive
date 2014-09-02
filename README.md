# Where old repos go to wither and die

To create a bundle for some repo:
```
$ git bundle create ../archive/BUNDLE_NAME.bundle master [branch1 [[branch2] [etc..]]]
```

List refs in bundle
```
$ git ls-remote ../archive/BUNDLE_NAME.bundle
```

To revive a repo, treat the bundle just like a remote, using fetch
```
$ git fetch ../archive/BUNDLE_NAME.bundle refs/heads/\*:refs/remotes/bundle/\*
```

