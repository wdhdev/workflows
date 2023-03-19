## [do-not-merge](https://github.com/wdhdev/workflows/blob/main/do-not-merge.yml)
If a pull request is labelled `do not merge`, this workflow will automatically run and fail, so maintainers cannot merge it.

**Setup**:
- Branch Protection
  - Set `Do Not Merge` as a required workflow to merge.
- Create Label
  - Create a label called `do not merge`.

## [publish-npm-package](https://github.com/wdhdev/workflows/blob/main/publish-npm-package.yml)
Publish a new release of an npm package when a new release is made in your repository.

**Required Secrets**:
- `NPM_TOKEN` - Your npm access token. You can learn to create one [here](https://docs.npmjs.com/about-access-tokens).
  - Make sure you use a legacy token and the type is automated.
