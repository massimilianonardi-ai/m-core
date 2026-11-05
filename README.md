# m-core

Independent, real source package of shared technical shell libraries used by
`m-term` and `m-rsudo`, with the package-local `readpass` and `ssh-askpass`
commands. The `m-os` bootstrap, `core.lib.sh`, state and `pkg` remain in
`m-os` and are not copied here.

`v0.1.0` is a published, checksum-protected GitHub release built by
`sh build.sh release`. Its archive contains `bin/`, `lib/sh/` and
`res/manual/` from actual owned sources. `pkg-catalog/pkg-schema-v2` owns the
corresponding `m-core` definition and `link/lib/sh` projections.

The libraries are **package-local**. After installing their exact concrete
through the public `m pkg` command, a shell must select it through
`context pkg=m-core@v0.1.0` before using the public POSIX dot-source
surface, e.g. `. array.lib.sh`. Do not duplicate these libraries into
`m-os/lib/sys/sh` or redefine `loadsyslib`.

The real composed `m-core`/`m-term`/`m-rsudo` install and library/command
smoke has passed on a GitHub-hosted Ubuntu runner. This does **not** establish
an interactive terminal, remote privileged SSH, or stable physical-host PASS.
