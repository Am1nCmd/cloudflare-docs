---
_build:
  publishResources: false
  render: never
  list: never

name: "Don't throw from async functions"
date: "2022-10-10"
enable_flag: "capture_async_api_throws"
disable_flag: "do_not_capture_async_api_throws"
---

If an async function throws an error, the function should return a promise which should reject, rather than ever itself ever thrown an error synchronously. The `capture_async_api_throws` compatibility flag will ensure that async functions will conform to this standard behavior, only ever rejecting and never throwing any errors synchronously.
