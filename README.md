# action-ghrelease

Fork and enhance from original repository: https://github.com/softprops/action-gh-release

Check `action.yml` for inputs

### Sample usage
```yaml
  - name: create release with assests
    if: ${{env.VERSION}}
    continue-on-error: true
    uses: phuonghuynh/action-ghrelease@v1.1.0
    env:
      GITHUB_TOKEN: ${{env._GITHUB_PAT}}
    with:
      repository: phuonghuynh/testci3
      commitish: main
      tag_name: ${{env.RELEASE_TAG}}
      name: Release ${{env.RELEASE_TAG}}
      #          body: Auto release API ${{env.RELEASE_TAG}} by @ci
      files: ${{env.TARBALL}}
```
