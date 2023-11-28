cargo-criterion-means
==========

Command-line program to gather the mean and standard error values
from criterion benchmarks.

Install
-------

```bash
cargo install cargo-criterion-means
```

Run
-------

```bash
cargo criterion-means [optional path to project root]
```

Output
-------

It sends comma-delimited text to standard out. For example:

```text
Group,Id,Mean(ns),StdErr(ns)
compare_is_consecutive,regular/avx2,3.0443,0.0080137
compare_is_consecutive,regular/avx512f,3.0232,0.0023419
compare_is_consecutive,regular/sse2,3.0785,0.0016257
compare_is_consecutive,regular2/sse2,4.3907,0.0038452
compare_is_consecutive,rotate/avx2,1.3775,0.0039389
compare_is_consecutive,rotate/avx512f,1.2408,0.0060673
compare_is_consecutive,rotate/sse2,1.996,0.0055311
```

You can then analyze and tabulate via a spreadsheet (pivot tables work great) or via a dataframe library such as `Polars`.
