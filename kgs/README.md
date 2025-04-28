# kgs

This is the Panoma / Hugoton dataset from KGS, as used in [the SEG machine learning contest in 2016](https://github.com/seg/2016-ml-contest).

For teaching about data science, Pandas, etc, you probably want the 'raw' files, all contained in `panoma_data.xlsx` as sheets. The sheets are broken out in:

- `panoma_data__data.csv` — The actual data
- `panoma_data__wells.csv` — The locations and completion dates of the wells
- `panoma_data__facies.csv` — The mapping from 'facies' codes to lithology
- `panoma_data__columns.csv` — Descriptions of the features in the data

The file `panoma-training-data.csv` contains everything, including some computed columns. This is the result of doing some manipulation, and is an example of what a student might make in a class.
