# Ruby on Rails Linters

If you are not familiar with linters and GitHub Actions, read [root level README](../README.md).

## Set-up GitHub Actions


This GitHub Action is going to run [Rubocop](https://docs.rubocop.org/en/stable/) to help you find style/linter issues.

[Rubocop](https://docs.rubocop.org/en/stable/) is a Ruby static code analyzer (a.k.a. linter) and code formatter. It will enforce many of the guidelines outlined in the community [Ruby Style Guide](https://rubystyle.guide/).

Please do the following **steps in this order**:

1. In the first commit of your feature branch create a `.github/workflows` folder and add a copy of [`.github/workflows/linters.yml`](.github/workflows/linters.yml) to that folder.
2. When you open your first pull request you should see the result of the GitHub Actions.
3. Click on the `Details` link to see the full output and the errors that need to be fixed.

## Set-up linters in your local env

1. Add this line to the `Gemfile`
    ```
    gem 'rubocop', '>= 1.0', '< 2.0'
    ```
2. Run `bundle install`.
3. Copy [.rubocop.yml](./.rubocop.yml) to the root directory of your project
5. Run `rubocop`.
6. Fix linter errors `rubocop --fix`.