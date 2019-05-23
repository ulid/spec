<h1 align="center">
	<br>
	<br>
	<img width="360" src="logo.png" alt="ulid">
	<br>
	<br>
	<br>
</h1>

# Universally Unique Lexicographically Sortable Identifier

UUID can be suboptimal for many use-cases because:

- It isn't the most character efficient way of encoding 128 bits of randomness
- UUID v1/v2 is impractical in many environments, as it requires access to a unique, stable MAC address
- UUID v3/v5 requires a unique seed and produces randomly distributed IDs, which can cause fragmentation in many data structures
- UUID v4 provides no other information than randomness which can cause fragmentation in many data structures

Instead, herein is proposed ULID:

```javascript
ulid() // 01ARZ3NDEKTSV4RRFFQ69G5FAV
```

- 128-bit compatibility with UUID
- 1.21e+24 unique ULIDs per millisecond
- Lexicographically sortable!
- Canonically encoded as a 26 character string, as opposed to the 36 character UUID
- Uses Crockford's base32 for better efficiency and readability (5 bits per character)
- Case insensitive
- No special characters (URL safe)
- Monotonic sort order (correctly detects and handles the same millisecond)

## Implementations in other languages

From ourselves and the community!

| Language | Author | Binary Implementation |
| -------- | ------ | --------------------- |
| [C++](https://github.com/suyash/ulid) | [suyash](https://github.com/suyash) | ✓ |
| [C#](https://github.com/mcb2001/CSharp.Ulid) | [mcb2001](https://github.com/mcb2001) |
| [Clojure](https://github.com/theikkila/clj-ulid) | [theikkila](https://github.com/theikkila) |
| [Objective-C](https://github.com/whitesmith/ulid) | [ricardopereira](https://github.com/ricardopereira) |
| [Crystal](https://github.com/SuperPaintman/ulid) | [SuperPaintman](https://github.com/SuperPaintman) |
| [Dart](https://github.com/agilord/ulid) | [isoos](https://github.com/isoos) | ✓ |
| [Dart](https://github.com/GuepardoApps/d-ulid) | [GuepardoApps](https://github.com/GuepardoApps) |
| [Delphi](https://github.com/martinusso/ulid) | [matinusso](https://github.com/martinusso) |
| [D](https://github.com/enckse/ulid) | [enckse](https://github.com/enckse) |
| [D (dub)](https://code.dlang.org/packages/ulid-d) | [extrawurst](https://github.com/Extrawurst)
| [Erlang](https://github.com/savonarola/ulid) | [savonarola](https://github.com/savonarola) |
| [Elixir](https://github.com/Homepolish/ulid) | [Homepolish](https://github.com/Homepolish) | ✓ |
| [Elixir](https://github.com/merongivian/ulid) | [merongivian](https://github.com/merongivian) |
| [Elixir](https://github.com/omisego/ex_ulid) | [omisego](https://github.com/omisego) | ✓ |
| [Elixir (Ecto)](https://github.com/TheRealReal/ecto-ulid) | [dcuddeback](https://github.com/dcuddeback) | ✓ |
| [F#](https://github.com/lucasschejtman/FSharp.Ulid) | [lucasschejtman](https://github.com/lucasschejtman) |
| [Factor](https://github.com/AlexIljin/ulid) | [Alexander Ilin](https://github.com/AlexIljin) | ✓ |
| [Go](https://github.com/oklog/ulid) | [oklog](https://github.com/oklog) | ✓ |
| [Haskell](https://github.com/steven777400/ulid) | [steven777400](https://github.com/steven777400) | ✓ |
| [Java](https://github.com/huxi/sulky/tree/master/sulky-ulid) | [huxi](https://github.com/huxi) | ✓ |
| [Java](https://github.com/azam/ulidj) | [azam](https://github.com/azam) |
| [Java](https://github.com/Lewiscowles1986/jULID) | [Lewiscowles1986](https://github.com/Lewiscowles1986) |
| [JavaScript](https://github.com/ulid/javascript) | [ulid](https://github.com/ulid) |
| [JavaScript](https://github.com/aarondcohen/id128) | [aarondcohen](https://github.com/aarondcohen) | ✓ |
| [Julia](https://github.com/ararslan/ULID.jl) | [ararslan](https://github.com/ararslan) |
| [Kotlin](https://github.com/GuepardoApps/kULID) | [GuepardoApps](https://github.com/GuepardoApps) |
| [Lua](https://github.com/Tieske/ulid.lua) | [Tieske](https://github.com/Tieske) |
| [.NET](https://github.com/RobThree/NUlid) | [RobThree](https://github.com/RobThree) | ✓ |
| [.NET](https://github.com/fvilers/ulid.net) | [fvilers](https://github.com/fvilers)
| [Nim](https://github.com/adelq/ulid) | [adelq](https://github.com/adelq)
| [OCaml](https://github.com/stripedpajamas/ocaml-ulid) | [stripedpajamas](https://github.com/stripedpajamas) |   |
| [Perl 5](https://github.com/bk/Data-ULID) | [bk](https://github.com/bk) | ✓ |
| [PHP](https://github.com/Lewiscowles1986/ulid) | [Lewiscowles1986](https://github.com/Lewiscowles1986) |
| [PHP](https://github.com/robinvdvleuten/php-ulid) | [robinvdvleuten](https://github.com/robinvdvleuten) |
| [PowerShell](https://github.com/PetterBomban/posh-ulid) | [PetterBomban](https://github.com/PetterBomban) |
| [Python](https://github.com/mdipierro/ulid) | [mdipierro](https://github.com/mdipierro) |
| [Python](https://github.com/ahawker/ulid) | [ahawker](https://github.com/ahawker) | ✓ |
| [Python](https://github.com/mdomke/python-ulid) | [mdomke](https://github.com/mdomke) | ✓ |
| [R](https://github.com/hrbrmstr/ulid) | [hrbrmstr](https://github.com/hrbrmstr) |   |
| [Ruby](https://github.com/rafaelsales/ulid) | [rafaelsales](https://github.com/rafaelsales) |
| [Rust](https://github.com/mmacedoeu/rulid.rs) | [mmacedoeu](https://github.com/mmacedoeu) | ✓ |
| [Rust](https://github.com/dylanhart/ulid-rs) | [dylanhart](https://github.com/dylanhart) | ✓ |
| [Scala](https://github.com/petitviolet/ulid4s) | [petitviolet](https://github.com/petitviolet) |
| [SQL-Microsoft](https://github.com/rmalayter/ulid-mssql) | [rmalayter](https://github.com/rmalayter) | ✓ |
| [Swift](https://github.com/simonwhitehouse/ULIDSwift) | [simonwhitehouse](https://github.com/simonwhitehouse) |
| [Swift](https://github.com/yaslab/ULID.swift) | [yaslab](https://github.com/yaslab) | ✓ |
| [Tcl](https://wiki.tcl-lang.org/48827) | [dbohdan](https://github.com/dbohdan) |

## Specification

Below is the current specification of ULID as implemented in [ulid/javascript](https://github.com/ulid/javascript).

*Note: the binary format has not been implemented in JavaScript as of yet.*

```
 01AN4Z07BY      79KA1307SR9X4MV3

|----------|    |----------------|
 Timestamp          Randomness
   48bits             80bits
```

### Components

**Timestamp**
- 48 bit integer
- UNIX-time in milliseconds
- Won't run out of space 'til the year 10889 AD.

**Randomness**
- 80 bits
- Cryptographically secure source of randomness, if possible

### Sorting

The left-most character must be sorted first, and the right-most character sorted last (lexical order). The default ASCII character set must be used. Within the same millisecond, sort order is not guaranteed

### Canonical String Representation

```
ttttttttttrrrrrrrrrrrrrrrr

where
t is Timestamp (10 characters)
r is Randomness (16 characters)
```

#### Encoding

Crockford's Base32 is used as shown. This alphabet excludes the letters I, L, O, and U to avoid confusion and abuse.

```
0123456789ABCDEFGHJKMNPQRSTVWXYZ
```

### Monotonicity

When generating a ULID within the same millisecond, we can provide some
guarantees regarding sort order. Namely, if the same millisecond is detected, the `random` component is incremented by 1 bit in the least significant bit position (with carrying). For example:

```javascript
import { monotonicFactory } from 'ulid'

const ulid = monotonicFactory()

// Assume that these calls occur within the same millisecond
ulid() // 01BX5ZZKBKACTAV9WEVGEMMVRZ
ulid() // 01BX5ZZKBKACTAV9WEVGEMMVS0
```

If, in the extremely unlikely event that, you manage to generate more than 2<sup>80</sup> ULIDs within the same millisecond, or cause the random component to overflow with less, the generation will fail.

```javascript
import { monotonicFactory } from 'ulid'

const ulid = monotonicFactory()

// Assume that these calls occur within the same millisecond
ulid() // 01BX5ZZKBKACTAV9WEVGEMMVRY
ulid() // 01BX5ZZKBKACTAV9WEVGEMMVRZ
ulid() // 01BX5ZZKBKACTAV9WEVGEMMVS0
ulid() // 01BX5ZZKBKACTAV9WEVGEMMVS1
...
ulid() // 01BX5ZZKBKZZZZZZZZZZZZZZZX
ulid() // 01BX5ZZKBKZZZZZZZZZZZZZZZY
ulid() // 01BX5ZZKBKZZZZZZZZZZZZZZZZ
ulid() // throw new Error()!
```

#### Overflow Errors when Parsing Base32 Strings

Technically, a 26-character Base32 encoded string can contain 130 bits of information, whereas a ULID must only contain 128 bits. Therefore, the largest valid ULID encoded in Base32 is `7ZZZZZZZZZZZZZZZZZZZZZZZZZ`, which corresponds to an epoch time of `281474976710655` or `2 ^ 48 - 1`.

Any attempt to decode or encode a ULID larger than this should be rejected by all implementations, to prevent overflow bugs.

### Binary Layout and Byte Order

The components are encoded as 16 octets. Each component is encoded with the Most Significant Byte first (network byte order).

```
0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                      32_bit_uint_time_high                    |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|     16_bit_uint_time_low      |       16_bit_uint_random      |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                       32_bit_uint_random                      |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                       32_bit_uint_random                      |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
```

## Prior Art

Partly inspired by:
- http://instagram-engineering.tumblr.com/post/10853187575/sharding-ids-at-instagram
- https://firebase.googleblog.com/2015/02/the-2120-ways-to-ensure-unique_68.html
