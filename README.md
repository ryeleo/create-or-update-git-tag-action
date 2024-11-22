[![Test](https://github.com/snow-actions/composite-action-template/actions/workflows/test.yml/badge.svg)](https://github.com/snow-actions/composite-action-template/actions/workflows/test.yml)

# Composite Action `create-or-update-git-tag-action`

Create or update a git tag.
Only update the git tag if the message of the git tag is changed.

This is useful if you are trying to store some data within a git tag message.

NOTE: Will force update the git tag if an update is required.

## Usage

```yml
steps:
  - uses: actions/checkout@v4
  - uses: ryeleo/create-or-update-git-tag-action@main
    with:
      tag-name: tag-name
      tag-message: my message
```

## Inputs

See [action.yml](action.yml)

| Name | Description  | Required |
| - | - | - | - |
| `tag-name` | Tag to be created or updated.  | yes |
| `tag-message` | Message to be set for the tag. | yes |

## Supported

### Runners

<!-- TODO
- `ubuntu-*`
- `windows-*`
- `macos-*`
-->
- `self-hosted`

### Events

- Any

## Dependencies

- Bash
- [actions/checkout](https://github.com/actions/checkout)
