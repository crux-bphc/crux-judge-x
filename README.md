# crux-judge-x

## Contributing

We love contributions and would be glad to help you make good patches. That out of the way, an average
contribution would involve the following:

1. Fork this repository in your account.
2. Clone it on your local machine.
3. Add a new remote using `git remote add upstream https://github.com/crux-bphc/crux-judge-x.git`.
4. Create a new feature branch with `git checkout -b my-feature`.
5. Make your changes.
6. Commit your changes.
7. Rebase your commits with `upstream/master`:
  - `git checkout master`
  - `git fetch upstream master`
  - `git reset --hard FETCH_HEAD`
  - `git checkout my-feature`
  - `git rebase master`
8. Resolve any merge conflicts, and then push the branch with `git push origin my-feature`.
9. Create a Pull Request detailing the changes you made and wait for review/merge.

It might seem a little complicated at a glance, but the fundamental concept is simple: we want to ensure that your changes are always made on top of the latest changes to the project and thus, we can easily merge your code. If you are facing any troubles, create a PR as you usually would and we would merge it manually. :)

### Commit Message Guidelines

The commit message:

- is written in the imperative (e.g., "Fix ...", "Add ...")
- is kept short (less than 80 characters), while concisely explaining what the commit does.
- is clear about what part of the code is affected -- often by prefixing with the name of the subsystem and a colon, like "express: ..." or "docs: ...".
- does not end with a period.
- if needed, should have a multiline description as well.
- if needed, should contain a reference to the relevant issue/PRs on a separate line.

Good summaries:

- `scripts: Fix running celery and django tests individually.`
- `create_user: Fix exception handling bad input.`
- `Add Google OAuth integration.`

Compare `create_user: Fix exception handling bad input.` with:

- `create_user was broken`, which doesn't explain how it was broken (and isn't in the imperative)
- `Fix exception when given bad input`, in which it's impossible to tell from the summary what part of the code is affected
- `create_user: Fixing exception when given bad input.`, not in the imperative
- `create_user: Fixed exception when given bad input.`, not in the imperative

An example of a longer commit message that closes a GitHub issue would be:

```
typeahead: Show typeahead only if cursor is before space or punctiation.

This solves the issue with typeahead appearing in the middle of an
already-completed typeahead word.

Example: Earlier, '@ran|dom' would also trigger the typeahead and show
'random', but selecting it would turn it into '@**random** dom'.

We still have a problem to solve of preventing typeahead from
appearing on a space in the middle of an already-completed typeahead
word, but that is its own independent bug.

Fixes #7283.
```

## License

This software is released under the MIT License.

```
Copyright 2018 Crux

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```