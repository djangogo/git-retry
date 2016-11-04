git-retry(1)
============

`git retry` is a bootstrap that wraps a standard `git` command execution in a
fault-tolerant retry wrapper. If a retry succeeds, the return code of the
successful attempt is returned. Otherwise, the return code of the last failed
attempt is returned. The wrapper is aware of `git`-specific failure conditions
and will only consider retrying if a given failure can be linked to such a
condition.

Part of the chromium **depot\_tools** suite. These tools are meant to assist
with the development of chromium and related projects. Download the tools from
[here](https://chromium.googlesource.com/chromium/tools/depot\_tools.git).
