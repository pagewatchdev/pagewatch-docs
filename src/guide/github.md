# GitHub

## Continuous integration with GitHub

You can run PageWatch as part of your continuous integration process.  On every pull request or deploy you'll be able to test your site and catch any issues before it becomes an issue.

![An image](./github-checks.png)

## Installation

### 1: Install the GitHub app 

[Install the GitHub app from your account](https://app.pagewatch.dev/admin/admin/integrations)

Make sure you give the app permissions to the relevant repository.

### 2: Use the API to run the audit and report results
::: tip
This works automatically if you make use of the [Netlify plugin.](https://docs.pagewatch.dev/guide/netlify.html)
:::

To report the details to an pull request run, you have to include the following fields when running an audit from the API

```
commit_hash,  // the git ref for the build
repo_url,  // the full github repo url
pull_request: true  // specify that this build was started from a pull request
```

See the [api documentation](https://docs.pagewatch.dev/guide/api.html) for detailed information.
