# Tsampi 0000 - null byte edition

Tsampi is a federated permissioned blockchain.
This is the first public testnet.

## The Rules

1. 0 files may be deleted
1. 0 files may be edited
1. 1 file must be created unless it is a merge commit then no files can be created
1. a file must be named the hexdigest of the sha1 of its contents  with the extension `.md` and within the `./data` directory
  * `sha1sum ./data/adc83b19e793491b1c6ea0fd8b46cd9f32e592fc.md
  adc83b19e793491b1c6ea0fd8b46cd9f32e592fc  ./data/adc83b19e793491b1c6ea0fd8b46cd9f32e592fc.md`
1. the file contents must be utf8 encoded
1. a commit hash must have proper proof-of-work
  * `uint(COMMIT_HASH) < (3 / git show --format=raw --show-signature | wc -c ) * 0XFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF`
1. all commits must be valid relative all their respective immediate parents commits
1. the rules may be broken if the commit is signed with gpg fingerprint `8C2E 500D 0D00 45B5 0DB6  2786 7CDA 9DF0 F5CF 98B9`
