# :icon-home: Welcome to Wraph

Wraph is a software tool. It provides a Wrapping Graph that aggregates multiple APIs.
It's aim is to simplify the integration of multiple APIs under a single point of access.
This single point of access provides added benefits:

- Secure
- Observable
- Auditable

It's blazing fast and doesn't crash, it's written in Rust.

### :icon-lock: Secure

It's possible to control access to the whole API in a single point.
After that initial control the security can also be delegated (inherited) by each API. This allows the creators of each API to have their own controls and not have to change their security policies.

### :icon-eye: Observable

A single point of access to all the APIs provides a single place where performance of the whole Wraph and each single API can be measured.

### :icon-codescan-checkmark: Auditable

Traces of each access can be obtained and linked to software clients of the information. This provides full auditability of all the accesses to the Wraph and all the underlying APIs.
