# c-nstd <!-- omit from toc -->
C non-standard library

Defines a non-standard (custom) implementation for C.

___

- [Types](#types)
___

# Types

Types in `c-nstd` are straight to the point, they follow the convention: `[<prefix>_]<base><size>[<qualifier>]_<construct>`.

i.e. `u32c_t` would be `unsigned int const` with the `_t` denoting the entity is a primitive data type

**Segment**     | Description                 | Example
 :------------: | :-------------------------- | :----------------------------------------------
`[<prefix>]`    | simply put, the prefix name | `reg_` register, `adr_` address
`<base>`        | base (core) data type       | `u` unsigned, `s` signed, `f` float
`<size>`        | size of the type in bits    | `8` bits, `16` bits, `32` bits, `64`bits
`[<qualifier>]` | optional variable qualifier | `c` const, `v` volatile
`_<construct>`  | programming construct       | `_t` primitive type, `_s` struct, `_u` union, `_e` enum, `_p` pointer

**Exceptions**:
 - `void *` is denoted as `v0_p`, since the size cannot be defined until compilation.
 -