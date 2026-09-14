# snapshot

Deterministic snapshot assertions for bytes, JSON, and Object values.

```text
cpm install snapshot@1.0.0
```

```celest
import "snapshot";
snapshot.match("response", response.body);
snapshot.json("metadata", value);
```

`match` compares bytes with a named snapshot, `equal` compares ordinary values, `json` canonicalizes JSON values, and `object` snapshots public Object properties. A mismatch throws with the snapshot name and deterministic actual value. The package never updates files implicitly; fixture creation or replacement belongs to the caller's test workflow. Inputs are borrowed during serialization, and platform-dependent values must be normalized by the test before comparison.
