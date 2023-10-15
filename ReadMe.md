[πανταρει](https://en.wikipedia.org/wiki/Heraclitus#Panta_rhei,_%22everything_flows%22).py [![Unlicensed work](https://raw.githubusercontent.com/unlicense/unlicense.org/master/static/favicon.png)](https://unlicense.org/)
===========
~~[wheel (GHA via `nightly.link`)](https://nightly.link/KOLANICH-libs/pantarei.py/workflows/CI/master/urm-0.CI-py3-none-any.whl)~~
~~![GitLab Build Status](https://gitlab.com/KOLANICH/pantarei.py/badges/master/pipeline.svg)~~
~~![GitLab Coverage](https://gitlab.com/KOLANICH/pantarei.py/badges/master/coverage.svg)~~
~~[![GitHub Actions](https://github.com/KOLANICH-libs/pantarei.py/workflows/CI/badge.svg)](https://github.com/KOLANICH-libs/pantarei.py/actions)~~
[![N∅ hard dependencies](https://shields.io/badge/-N∅_Ъ_deps!-0F0)
[![Libraries.io Status](https://img.shields.io/librariesio/github/KOLANICH-libs/pantarei.py.svg)](https://libraries.io/github/KOLANICH/pantarei.py)
[![Code style: antiflash](https://img.shields.io/badge/code%20style-antiflash-FFF.svg)](https://codeberg.org/KOLANICH-tools/antiflash.py)

**We have moved to https://codeberg.org/KAbs/pantarei.py (the namespace was changed to `KAbs`, which groups abstraction layers), grab new versions there.**

Under the disguise of "better security" Micro$oft-owned GitHub has [discriminated users of 1FA passwords](https://github.blog/2023-03-09-raising-the-bar-for-software-security-github-2fa-begins-march-13/) while having commercial interest in success and wide adoption of [FIDO 1FA specifications](https://fidoalliance.org/specifications/download/) and [Windows Hello implementation](https://support.microsoft.com/en-us/windows/passkeys-in-windows-301c8944-5ea2-452b-9886-97e4d2ef4422) which [it promotes as a replacement for passwords](https://github.blog/2023-07-12-introducing-passwordless-authentication-on-github-com/). It will result in dire consequencies and is competely inacceptable, [read why](https://codeberg.org/KOLANICH/Fuck-GuanTEEnomo).

If you don't want to participate in harming yourself, it is recommended to follow the lead and migrate somewhere away of GitHub and Micro$oft. Here is [the list of alternatives and rationales to do it](https://github.com/orgs/community/discussions/49869). If they delete the discussion, there are certain well-known places where you can get a copy of it. [Read why you should also leave GitHub](https://codeberg.org/KOLANICH/Fuck-GuanTEEnomo).

---

Just an abstraction layer around various progress reporters.

When making a lib/tool doing long operations we have several options:

1. Not to show progress at all. Pro: no code for that. Con: No progress.
2. Take a dependency on a specific lib to show fancy progress. Pro: Fancy progress. Con: A dependency on a specific lib. A user can say "I can't install that lib on my PC, I prefer another one. Don't force me to install that shit".
3. Inline an existing lib. The same drawbacks like in 2., but also code bloat and a try to cheat the user.
4. Create an own small and simple progress visualizer and inline it. Pro: some progress report. Con: code bloat and the report is not fancy.
5. Create a **small** and **simple** abstraction layer on different popular reporters (that it is likely that at least one of them is already present on user's machine) and use it. **This library does this.** Pro: fancy progress reports, not enforcing a single dependency. Con: dependency on the abstraction layer itself.
