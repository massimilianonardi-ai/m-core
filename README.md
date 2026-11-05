# m-core

Source repository for shared technical `m` commands and libraries required by the extracted terminal/menu and `rsudo` capabilities but not already part of the autonomous `m-os` baseline: generic container/encoding/random/IPC/SSH and injection libraries plus the required credential-input helpers. Current source files and operational manuals are imported intact.

The authoritative `m` bootstrap, shell core, `pkg`, state and resource runtime remain in `m-os` rather than being duplicated here. A future real `pkg` v2 composition must resolve shell-library loading against installed package views and verify real consumers; copying the source layout is not evidence of that working.
