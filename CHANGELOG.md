### Version 1.0.0-rc.2

#### Major Development
- None

#### API Changes
- None

#### Bug Fixes
- `Connect()` only returns successfully if both Chat and Events are authenticated, and fails silently in all other instances.
    - `Connect()` now succeeds in instances where only Chat or Events are authenticated (where applicable)
    - Failure is only invoked if no authentication at all has taken place prior to being called
    - Function no longer silently fails, always triggering an `onSuccess` or `onFailed` callback

---

### Version 1.0.0-rc.1

#### Major Development
- None

#### API Changes
- None

#### Bug Fixes
- Cached tokens are only refreshed during `Authenticate` calls, resulting in invalidated tokens over extended periods of time.
  - All API calls now respond to a *401 Unauthorized* response from the server
  - Tokens are refreshed and the API call re-attempted before failure state is returned
  - Refreshed tokens are stored in the same way as the `Authenticate` calls for use in future API calls

---

### Version 1.0.0

#### Major Development
- Initial release for Unreal Engine 5

#### API Changes
- None

#### Bug Fixes
- None
