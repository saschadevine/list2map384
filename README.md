# list2map384.py
# SLD 2025

## License
```
This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```

## Purpose
```list2map384.py``` generates a 16x24 map (XLSX) from a list of 384 indices and associated identities (CSV)

## Example Applications
- Generate a 384w plate map of compound stocks from a linear list of compound stocks outputted by compound management software (e.g., Mosaic)
- Generate a 384w plate map of data from a linear list of readings outputted by a plate reader or qPCR instrument

## Requirements
```listmap384.py``` requires:
- Python 3.10.12 or better
- ```openpyxl```

## Command Line Syntax
```
python3 list2map384.py INPUT_CSV_FILENAME
```

## Assumptions
- INPUT_CSV_FILENAME refers to a CSV file
- Output is templated on the included ```template.xlsx``` and its name is derived from INPUT_CSV_FILENAME (```MAP__CSV_FILE_NAME```)
- INPUT_CSV_FILENAME contains exactly 385 lines
  - First line: labels
  - Subsequent lines: data
  - All data is associated with one map ID
- Each line of INPUT_CSV_FILENAME contains the following (at minimum):
  - Map ID (by default, ```Plate Barcode```)
  - Map cell index (by default, ```Position```)
  - Map cell value  (by default, ```CompoundBatch```)
  - For alternative cell values, visit and edit the script appropriately
