---
_build:
  publishResources: false
  render: never
  list: never

name: "Don't substitute `null` on `TypeError`"
date: "2022-06-01"
enable_date: "2022-06-01"
enable_flag: "dont_substitute_null_on_type_error"
disable_flag: "substitute_null_on_type_error"
---

There was a bug in the runtime that meant that `null` values were occasionally substituted in when instead, a `TypeError` should have been thrown. The `dont_substitute_null_on_type_error` fixes this behavior so an error is correctly thrown instead, in these circumstances.
