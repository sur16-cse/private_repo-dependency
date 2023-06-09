# private_repo_dependency

### Hosted packages
specifying a dependency:
```
  dependencies:
  transmogrify: ^1.0.0
```

## To specify a source that isn’t pub.dev, use sdk, hosted, git, or path

code uses path to tell pub to get transmogrify from a local directory:
```
dependencies:
  transmogrify:
    path: /Users/me/transmogrify
```

If you want to use your own package repository, you can use hosted to specify its URL. The following YAML code creates a dependency on the transmogrify package using the hosted source.
```
environment: 
  sdk: >=2.15.0 < 3.0.0

dependencies:
  transmogrify:
    hosted: https://some-package-server.com
    version: ^1.4.0
```

## Git packages
 package is found using Git, and the URL after that is the Git URL that can be used to clone the package.
 ```
 dependencies:
  kittens:
    git: https://github.com/munificent/kittens.git
 ```
 
 if the package repo is private, if you can connect to the repo using SSH, then you can depend on the package by using the repo’s SSH URL:
 ```
 dependencies:
  kittens:
    git: git@github.com:munificent/kittens.git
 ```
depend on a specific commit, branch, or tag, add a ref key to the description:
```
dependencies:
  kittens:
    git:
      url: git@github.com:munificent/kittens.git
      ref: some-branch
```

Pub assumes that the package is in the root of the Git repository. To specify a different location in the repo, specify a path relative to the repository root:
```
dependencies:
  kittens:
    git:
      url: git@github.com:munificent/cats.git
      path: path/to/kittens
```

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
