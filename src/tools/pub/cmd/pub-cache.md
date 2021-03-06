---
title: dart pub cache
description: Use dart pub cache to manage your system cache.
toc: false
---

_Cache_ is one of the commands of the [pub tool](/tools/pub/cmd).

```
$ dart pub cache add <package> [--version <constraint>] [--all]
$ dart pub cache repair
```

The `dart pub cache` command works with the
[system cache](/tools/pub/glossary#system-cache).
To add new packages to your cache, use `dart pub cache add`.
To perform a clean reinstall of the packages in your system cache,
use `dart pub cache repair`.

## Options

For options that apply to all pub commands, see
[Global options](/tools/pub/cmd#global-options).

<dl>
<dt><code>add &lt;package&gt;</code></dt>
<dd>Installs a library in your cache.</dd>

<dt><code>--all</code></dt>
<dd>Optional. Use with <code>dart pub cache add</code> to install all
matching versions of a library.</dd>

<dt><code>--version &lt;constraint&gt;</code></dt>
<dd>Optional. Use with <code>dart pub cache add</code> to install the best
version matching the specified constraint. For example:

{% prettify nocode tag=pre+code %}
$ dart pub cache add http --version "0.12.2"
{% endprettify %}

If <code>--version</code> is omitted, pub installs the best of all known
versions.</dd>

<dt><code>repair</code></dt>
<dd>It's possible for packages in your pub cache to change or break.
For example, some editors make it easy to find implementation files for
packages in the pub cache, and you might accidentally edit one of those files.
The <code>dart pub cache repair</code> command performs a clean reinstall of all
hosted and git packages in the system cache.</dd>

<aside class="alert alert-info" markdown="1">
  *Problems?* See [Troubleshooting Pub](/tools/pub/troubleshoot).
</aside>