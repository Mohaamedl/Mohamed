# Mohamed
name: Full-year calendar
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.isocalendar.fullyear.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_isocalendar: yes
  plugin_isocalendar_duration: full-year
  name: "💫 Starlists"
category: github
description: This plugin displays your star lists.
examples:
  +repositories from star lists: https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.starlists.svg
  +languages from star lists: https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.starlists.languages.svg
index: 24
supports:
  - user
scopes: []
inputs:

  plugin_starlists:
    description: Enable starlists plugin
    type: boolean
    default: no

  plugin_starlists_limit:
    description: Display limit (star lists)
    type: number
    default: 2
    min: 1
    max: 100

  plugin_starlists_limit_repositories:
    description: Display limit (repositories per star list)
    type: number
    default: 2
    min: 0
    max: 100

  plugin_starlists_languages:
    description: Toggle star list languages statistics
    type: boolean
    default: no

  plugin_starlists_limit_languages:
    description: Disply limit (languages per star list)
    type: number
    default: 8
    min: 0
    zero: disable

  plugin_starlists_shuffle_repositories:
    description: Shuffle data for varied outputs
    type: boolean
    default: yes

  plugin_starlists_ignored:
    description: |
      Skipped star lists
      This is case and emojis insensitive
    type: array
    format: comma-separated
    default: ""
    example: 😎 list1, 🥳 list2, ...

  plugin_starlists_only:
    description:  |
      Restrict display to specified star lists
      This is case and emojis insensitive.
      This option is equivalent to `plugin_starlists_ignored` with all star lists but the ones listed in this option
    type: array
    format: comma-separated
    default: ""
    example: 😎 list1, 🥳 list2, ...
