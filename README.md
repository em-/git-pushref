# git-pushref

Push an arbitrary ref without checking out the repository.

Useful to skip CI when creating new branches on GitLab since
doing so with the API lacks the `ci.skip` option:
https://gitlab.com/gitlab-org/gitlab/-/issues/223698

## Usage

    ./git-pushref
        --url https://gitlab.com/emmh/git-pushref.git \
        --username oauth2 \
        --password 12345 \
        --hash 7c1178f3e740cbce2fa7a24f2911f383d6feae7b \
        --branch test \
        --option 'ci.variable="foo=bar"' \
        --option 'ci.variable="baz=quux"'

## License

MIT

## Related projects

* https://github.com/benhoyt/pygit - just enough git to create a repo and push to GitHub
