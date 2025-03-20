# Rock Property Catalog (RPC)

(This dataset was previously hosted on Subsurfwiki.org, no longer maintained.)

The RPC consists of:

- Mudrock Anisotropy, or — more appealingly — Mr Anisotropy. Compiled by Steve Horne, it contains over 1000 records of rocks, gathered from the literature. It is also public domain and carries only a disclaimer. But it's a spreadsheet, and emailing a spreadsheet around is not sustainable.
- The Common Ground database that was built by John A. Scales, Hans Ecke and Mike Batzle at Colorado School of Mines in the late 1990s, is now defunct and has been officially discontinued, as of September 2015. It contains over 4000 records, and is public domain. The trouble is, you have to restore a SQLite database to use it.

There are 5095 records in the main file; other files contain subsets of the data useful for teaching eg machine learning, eg see https://github.com/equinor/ml-pitfalls

This dataset carries a copyleft license: if you augment the dataset, you must push your changes back here &mdash; please make a PR. Thank you :)

### Datasets

* `rpc-2-simple.csv` — 2 features, 1 target of 2 classes: sand and shale only.
* `rpc-3-imbalanced.csv` — 440 rows, 3 features, 1 target of shale (200 rows), dolomite (200 rows) and limestone (40 rows, 12 with missing data)
* `rpc-3-simple-imbalanced.csv` — 372 rows, 2 features, 1 target of 3 classes: shale (200 rows), limestone (150 rows), and dolomite (20 rows).
* `rpc-4-lithologies.csv` — 800 rows, 3 features, 1 target of 4 classes: sand, shale, limestone and dolomite. Forty-eight 'limestone' rows have missing values for `Rho`.
* `rpc-CC-BY-SA.csv` — 5141 rows, many lithologies
