# action-ghrelease

Fork and enhance from original repository: https://github.com/softprops/action-gh-release

Check `action.yml` for inputs

### Sample usage
```yaml
  - name: create release with assests
    if: ${{env.VERSION}}
    continue-on-error: true
    uses: phuonghuynh/action-ghrelease@v0.2.1
    env:
      GITHUB_TOKEN: ${{env._GITHUB_PAT}}
      GITHUB_REF: ${{env.BRANCH}}
      GITHUB_REPOSITORY: phuonghuynh/testci3
    with:
      tag_name: ${{env.RELEASE_TAG}}
      name: Release ${{env.RELEASE_TAG}}
      body: Auto release API ${{env.RELEASE_TAG}} by @ci
      draft: false
      prerelease: false
      files: ${{env.TARBALL}}
```
