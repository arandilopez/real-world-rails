# Real World Rails

> Real World Rails applications and their open source codebases for developers to learn from

This is an actively maintained continuation of [eliotsykes/real-world-rails](https://github.com/eliotsykes/real-world-rails).

This project brings 200+ active, open source Rails apps and engines together in one repository. Having real production codebases aggregated in a single place has always been valuable for learning — but it's become dramatically more useful in the age of AI coding agents.

See [repos.md](repos.md) for the full list of included apps and engines with descriptions.

## Why this matters now

When this repo was created, you had to manually grep through code or use custom Ruby scripts to find patterns across apps. AI coding agents have changed that completely.

With all these codebases in one directory, you can point an agent at 200+ production Rails apps and ask questions like:

- "How do these apps implement background job retry logic?"
- "Show me every approach to multi-tenancy across these codebases"
- "What patterns do apps use for PDF generation?"
- "Find all the different ways these apps handle soft deletes"
- "Compare authentication implementations across apps using Devise vs. custom auth"

An agent can search, read, and cross-reference code across every app instantly — something that would have taken hours of manual work before. This makes real-world-rails one of the most practical resources for researching how production Rails apps actually solve problems.

### Storing your analyses

The `analyses/` directory is git-ignored — a safe place to store your own research:

- Markdown files, notes, pattern comparisons, or any documentation
- Won't be committed or show up in pull requests
- Keeps your workspace clean while working alongside the codebases

## Getting started

Ensure you have git-lfs installed: https://git-lfs.com

```bash
git clone git@github.com:steveclarke/real-world-rails.git
cd real-world-rails/
bin/setup
```

## Scripts

- **`bin/setup`** — Initialize and download all submodules (run after first clone)
- **`bin/update`** — Pull latest changes and update all submodules
- **`bin/status`** — Show how many apps are initialized

## Contributing

Contributions are welcome! If you know of a great open source Rails application or engine, please submit a pull request.

#### Criteria for adding apps

Apps should:
- Be open source and publicly available on GitHub
- Be built with Ruby on Rails
- Be actively maintained or represent quality code worth studying
- Be real-world applications (not just demos or tutorials)

#### How to add a Real World Rails app

Given a GitHub repo for a Rails app `githubuser/foo`:

```bash
GIT_LFS_SKIP_SMUDGE=1 git submodule add -b <DEFAULT_BRANCH> git@github.com:githubuser/foo.git apps/foo
```

#### How to remove a submodule

Only use this if a previously public repo has been removed:

```bash
git submodule deinit -f path/to/submodule
rm -rf .git/modules/path/to/submodule
git rm -f path/to/submodule
```

## Other Real World Codebase Collections

- [Real World Nuxt](https://github.com/steveclarke/real-world-nuxt)
- [Real World Ruby Apps](https://github.com/jeromedalbert/real-world-ruby-apps)
- [Real World Sinatra](https://github.com/jeromedalbert/real-world-sinatra)
- [Real World Django](https://github.com/ckrybus/real-world-django)
