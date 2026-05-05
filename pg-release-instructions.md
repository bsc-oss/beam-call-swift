# Release pg-call-swift
* start from main branch
* from pg-call:
    * `yarn run build:embedded`
    * `cp -r ./dist ./embedded/ios/Sources/dist/`
* from pg-call-swift: `rsync -a --delete --exclude .git ../pg-call/embedded/ios/ ./`
* adapt version in: `pg-call-swift/Sources/EmbeddedElementCall/EmbeddedElementCall.swift`
* `swift build` to test build
* `git commit -am "Release 0.0.2"`
* `git tag 0.0.2`
* `git push --tags`
* You can then undo the commit done on main as it is pushed and attached to the tag