# 7. Release Bugs

| Date | Phase |
| --- | --- |
|  February 24<sup>th</sup> | Release |

The magazine is happy with the work that has been done, but has asked that the songs picked for january appear on the home screen under the heading "Last Month's Favorites". Oh and by the way, John Lennon has been fired so please would you remove him from the application.

## :running: Activities

Follow along with the activities below to walk through the process of fixing issues in the release branch.

### 1 - Fix Issues in Feature Branches

__Developers__

Fetch the latest from origin and create a local tracking branch for the release:

```sh
$ git flow release pull v1.1.0
# checkout the release branch
Branch hotfix/YYYY-MM-DD set up to track remote branch release/1.1.0 from origin.
Switched to a new branch 'hotfix/YYYY-MM-DD'
```

Choose two developers to address each issue.

- Developer 1:
    1. Create a feature branch off of `release/1.1.0` named `last-months-favorites`.
    2. Commit the following changes to the feature branch:
        1. Create a section in [`/app/index.md`](/app/index.md) titled "Last Month's Favorites".
        2. Copy the text that was published last release and paste under "Last Month's Favorites". Be sure not to include John Lennon.

- Developer 2:
    1. Create a feature branch off of `release/1.1.0` named `remove-john-lennon`.
    2. Commit the following changes to the feature branch:
        1. Delete the file `/app/writer/john-lennon.md`.
        2. Remove references to John Lennon from [`/app/index.md`](/app/index.md)

Other team members may also choose an issue and make the changes themselves locally to gain more practice working in feature branches.

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 2 - Publish & Request to Merge Feature Branches

__Developers__

The two developers from the last step should now publish their feature branches to GitHub and open up Pull Requests against the `release/1.1.0` branch in the source repository:
```sh
$ git flow release publish v1.1.0
```

---

:cop: :raised_hand: - Please wait until everyone has caught up.

:construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction: :construction:

---

### 3 - Merge Feature Requests into Release Branch

__Maintainers__

Review the developer Pull Requests and merge them into `release/1.1.0`.

## Next

Finally, we will walk through the process of completing a release: merging into main, back down into develop, and creating a GitHub release tag.

[Go](8-completed-release.md)

## Quick Links

- [Readme](../readme.md)
- [1. Setup](1-setup.md)
- [2. Feature Branches](2-feature-branches.md)
- [3. Code Review](3-code-review.md)
- [4. Fetching the Latest](4-fetching-latest.md)
- [5. Hotfix](5-hotfix.md)
- [6. Release Branch](6-release-branch.md)
- [8. Completed Release](8-completed-release.md)
