Deleting from an **open addressing** hash table ([[Linear Probing]], [[Quadratic Probing]], [[Double Hashing]])

Can't just empty the bucket: a later search would hit the gap and stop early, missing keys further along the probe sequence

**Tombstone**: marker left in a bucket after deleting from it
- **search**: tombstone means keep probing
- **insert**: keep probing past it (to check the key isn't already there, so no **duplicates**), then put the new entry in the first tombstone found

Tombstones make probe sequences longer. Fixes:
- **local reorganisation**: after deleting, follow that key's probe sequence and move entries back into the freed bucket (doesn't work for every probing method)
- **rehash** periodically: reinsert everything into a fresh table, placing the most frequently used keys where they're quickest to find
