# list2map384
Generate a 16x24 map (XLSX) from a list of 384 indices and associated identities (CSV)

## Usage
```
python3 list2map384.py INPUT_CSV_FILENAME
```

## Expectations
- INPUT_CSV_FILENAME refers to a CSV file
- Output is XLSX format and its name is derived from INPUT_CSV_FILENAME (```MAP__CSV_FILE_NAME```)
- INPUT_CSV_FILENAME contains 385 lines
  - First line: labels
  - Subsequent lines: data
- Each line of INPUT_CSV_FILENAME contains the following (at minimum):
  - Value of cell in output  (by default, ```CompoundBatch```)
  - Plate ID (by default, ```Plate Barcode```)
  - Well ID (by default, ```Position```)
- 
