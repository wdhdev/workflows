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

## [sftp-deploy](https://github.com/wdhdev/workflows/blob/main/sftp-deploy.yml)
Deploy your changes to your server using SFTP, then restart the Docker container.

- This workflow was made for use with [Pterodactyl](https://pterodactyl.io)
- This workflow uses `SFTP`

**Required Secrets**:
- `SERVER` - The server IP or FQDN (Fully Qualified Domain Name).
  - This variable is used for deploying the changes and restarting the container.
- `FTP_PORT` - The port your SFTP server is running on.
- `FTP_USERNAME` - The SFTP username used for logging in.
- `FTP_PASSWORD` - The SFTP password user for logging in.
- `SSH_USERNAME` - The username used for logging into the server using SSH.
- `SSH_PASSWORD` - The password used for logging into the server using SSH.
- `CONTAINER` - The name of the Docker container which is being restarted.
