# Deployment Checklist

## GitHub Repository

1. Create a public repository named `mifanTeddy/status.mifan.im`.
2. Push this directory to the repository.
3. In GitHub repository settings, enable Actions workflow write permissions:
   `Settings -> Actions -> General -> Workflow permissions -> Read and write permissions`.
4. Run the `Setup CI` workflow manually once.
5. Set GitHub Pages to publish from the `gh-pages` branch after the first successful run.

## DNS

Create a CNAME record:

```text
status.mifan.im CNAME mifanTeddy.github.io
```

GitHub Pages will use the `cname: status.mifan.im` value from `.upptimerc.yml`.

## Optional Token

If workflow commits or issue updates fail with permission errors, create a classic GitHub token with `repo` and `workflow` scopes and save it as the repository secret `GH_PAT`.
