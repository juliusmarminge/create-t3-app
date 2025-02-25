# Contribution Guidelines

When contributing to `create-t3-app`, whether on GitHub or in other community spaces:

- Be respectful, civil, and open-minded.
- Before opening a new pull request, try searching through the [issue tracker](https://github.com/nexxeln/create-t3-app/issues) for known issues or fixes.

## How to Contribute

### Prerequisites

In order to not waste your time implementing changes that has already been declined, or is generally not needed, start by [opening an issue](https://github.com/t3-oss/create-t3-app/issues/new/choose) describing the problem you would like to solve.

### Setup your environment

_Some commands will assume you have the Github CLI installed, if you haven't, consider [installing it](https://github.com/cli/cli#installation), but you can always use the Web UI if you prefer that instead._

In order to contribute to this project, you will need to fork the repository:

```bash
gh repo fork t3-oss/create-t3-app
```

then, clone it to your local machine:

```bash
gh repo clone <your-github-name>/create-t3-app
```

This project uses [pnpm](https://pnpm.io) as its package manager. Install it if you haven't already:

```bash
npm install -g pnpm
```

Then, install the project's dependencies:

```bash
pnpm install
```

### Implement your changes

Now you're all setup and can start implementing your changes.

When you want to test your changes, run:

```bash
pnpm dev
```

which will build and start the CLI.

When making commits, make sure to follow the [convential commit](https://www.conventionalcommits.org/en/v1.0.0/) guidelines, i.e. prepending the message with `feat:`, `fix:`, `chore:` etc...

### When you're done

Check that your code follows the project's style guidelines by running:

```bash
pnpm check
```

Please also make a manual, functional test of your changes.

If your change should appear in the changelog, i.e. it changes some behavior of either the CLI or the outputted application, it must be captured by `changeset` which is done by running

```bash
pnpm changeset
```

and filling out the form with the appropriate information. Then, add the generated changeset to git:

```bash
git add ./changeset/*.md && git commit -m "chore: add changeset"
```

When all that's done, it's time to file a pull request to upstream:

```bash
gh pr create --web
```

and fill out the title and body appropriately. Again, make sure to follow the [convential commit](https://www.conventionalcommits.org/en/v1.0.0/) guidelines for your title.

## Credits

This documented was inspired by the contributing guidelines for [cloudflare/wrangler2](https://github.com/cloudflare/wrangler2/blob/main/CONTRIBUTING.md).
