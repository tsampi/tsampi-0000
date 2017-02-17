# Tsampi 0000 - null byte edition

Tsampi is a federated permissioned blockchain.
This is the first public testnet.

## How to post

1. Fork [https://github.com/tsampi/tsampi-0000/](https://github.com/tsampi/tsampi-0000/)
1. Clone your fork locally
1. Make a commit that follows the validation rules below
1. Push your commits to your fork
1. Make a Pull Request to merge your change back in to https://github.com/tsampi/tsampi-0000/
1. If your commits were all valid according to the rules, your PR will be accpeted.

## The Rules

1. 0 files may be deleted
1. 0 files may be edited
1. 1 file must be created unless it is a merge commit then no files can be created
1. a file must be named the hexdigest of the sha1 of its contents  with the extension `.md` and within the `./data` directory
  * `sha1sum ./data/adc83b19e793491b1c6ea0fd8b46cd9f32e592fc.md
  adc83b19e793491b1c6ea0fd8b46cd9f32e592fc  ./data/adc83b19e793491b1c6ea0fd8b46cd9f32e592fc.md`
1. the file contents must be utf8 encoded
1. a commit hash must have proper proof-of-work unless it is a merge commit
  * `uint(COMMIT_HASH) < (3 / git show --format=raw --show-signature | wc -c ) * 0XFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF`
1. all commits must be valid relative all their respective immediate parents commits
1. the rules may be broken if the commit is signed with gpg fingerprint<br>
  `8C2E 500D 0D00 45B5 0DB6  2786 7CDA 9DF0 F5CF 98B9`

## Pro Tip

Use https://gist.github.com/readevalprint/247e5d0b9090d43d1041b6d3450d4a36 to help find a valid commit
