# tetgen

Mirror of the latest stable version of `tetgen`. 

https://wias-berlin.de/software/tetgen/

### Pushing a new release

If the code is updated, a new release will be created automatically when a tag is pushed:

    git tag 1.x.y
    git push origin 1.x.y

This will trigger the github actions to build/upload the binaries for `tetgen`.
