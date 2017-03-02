## RF Git Process (aka RF Git Flow)

`master` represents the real-world state of the application. It is always in a deployable state. QA can count on this branch to test other applications against.

`release` represents the next release of the application. It has always been regression tested, but has not been verified on staging.

`develop` represents the future state of the application. It provides a common point for QA to run regression, but should never be referenced as a stable branch.

## Development on a feature branch:
Start a new feature branch from develop
Make commits on the feature branch
When work is ready for review, rebase your branch onto `develop` and create a pull request in github against `develop`
When review is complete and ready for merge to develop, merge your work into develop via a `--no-ff` merge
