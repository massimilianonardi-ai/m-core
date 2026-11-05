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
smoke passed on both GitHub-hosted Ubuntu and macOS in workflow
`massimilianonardi-ai/m-core` run `42037725004`. This does **not** establish
an interactive terminal, remote privileged SSH, or stable physical-host PASS.

Current main-source `loadlib_inject_stream` also accepts explicit
`--library reference local-source` inputs for selected package-owned shell
libraries, without changing bare system-library reference behavior. This
source change is not present in immutable `v0.1.0` and is available in the immutable v0.1.1 release; its installed consumer validation is tracked by R1.
