# Introduction #

The V8 release process is tightly connected to [Chrome's](https://www.chromium.org/getting-involved/dev-channel). The V8 team is using all four Chrome release channels to push new versions to the users.

If you want to look up what V8 version is in a Chrome release you can check [OmahaProxy](https://omahaproxy.appspot.com/). For each Chrome release a separate branch is created in the V8 repository to make the trace-back easier e.g. for [Chrome 45.0.2413.0](https://chromium.googlesource.com/v8/v8.git/+/chromium/2413).

# Canary releases #
Every day a new Canary build is pushed to the users via [Chrome's Canary channel](https://www.google.com/chrome/browser/canary.html?platform=win64). Normally the deliverable is the latest, stable enough version from [master](https://chromium.googlesource.com/v8/v8.git/+/roll).

Branches for a Canary normally look like this

```
remotes/origin/4.5.35
```

# Dev releases #
Every week a new Dev build is pushed to the users via [Chrome's Dev channel](https://www.google.com/chrome/browser/desktop/index.html?extra=devchannel&platform=win64). Normally the deliverable includes the latest stable enough V8 version on the Canary channel.

Branches for a Dev normally look like this

```
remotes/origin/4.5.35
```

# Beta releases #
Roughly every 6 weeks a new major branch is created e.g. [for Chrome 44](https://chromium.googlesource.com/v8/v8.git/+log/branch-heads/4.4). This is happening in sync with the creation of [Chrome's Beta channel](https://www.google.com/chrome/browser/beta.html?platform=win64). The Chrome Beta is pinned to the head of V8's branch. After approx. 6 weeks the branch is promoted to Stable.

Changes are only cherry-picked onto the branch in order to stabilize the version.

Branches for a Beta normally look like this

```
remotes/branch-heads/4.5
```

They are based on a Canary branch.

# Stable releases #
Roughly every 6 weeks a new major Stable release is done. No special branch is created as the latest Beta branch is simply promoted to Stable. This version is pushed to the users via [Chrome's Stable channel](https://www.google.com/chrome/browser/desktop/index.html?platform=win64).

Branches for a Beta normally look like this

```
remotes/branch-heads/4.5
```

They are promoted (reused) Beta branches