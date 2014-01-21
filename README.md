# platform-vms

Sometimes you write software meant to run on multiple architectures. Ideally, you could program, compile, debug, and test other architectures directly from yours. But that's currently not always (or remotely) true. This is a repository to make it easy to work with vms of various platforms. You might use it to do:

- user testing
- debugging
- compiling when cross-compilation [doesn't](https://code.google.com/p/go/issues/detail?id=6376) [work](https://www.google.com/search?q=cross-compilation+doesn%27t+work&oq=cross-compilation+doesn%27t+work&aqs=chrome..69i57.4420j0j7&sourceid=chrome&espv=210&es_sm=91&ie=UTF-8#q=cross+compile+doesn't+work).

## How does it work?

There's a bunch of [Vagrantfiles](http://docs.vagrantup.com/v2/vagrantfile/index.html), each specifying a vm, with a particular architecture, os, and installed stacks.

### Platforms supported

Breakdown by `arch` (really, os + arch), and by `stack`.
(All platforms include simple "base" stack).

```
├── amd64
│   └── linux_ubuntu
│       ├── base
│       └── go
└── i386
    └── linux_ubuntu
        ├── base
        └── go
```

### Platform wish list

Pull-requests welcome! If the platform you want isn't here, add it! (Or ask the community to add it.)

archs wanted:

- darwin amd64
  - golang
- darwin arm
- darwin i386
  - golang
- freebsd amd64
- freebsd arm
- freebsd i386
- linux arm
- windows amd64
- windows i386

stacks wanted:

- node
- python


## Install

1. [Install Virtualbox](https://www.virtualbox.org/wiki/Downloads)
1. [Install Vagrant](http://www.vagrantup.com/)
1. Install this repo:

    git clone https://github.com/jbenet/platform-vms

## Usage

    cd <arch>/<os>/<stack>
    vagrant up
    vagrant ssh
