# Datatypes supported by Firebird

## Text Types

| Name      | Size         | Range     | Description            |
|-----------|--------------|-----------|------------------------|
| CHAR(n)   | n characters | 1 - 32K   | Fixed length text      |
| VARCHAR(n)| n characters | 1 - 32K   | Variable length text   |

## Numeric Types

| Name      | Size   | Range                    | Description   |
|-----------|--------|--------------------------|---------------|
| SMALLINT  |        |                          |               |
| INTEGER   |        |                          |               |
| INT64     |        |                          |               |


| Name             | Size   | Range                    | Description   |
|------------------|--------|--------------------------|---------------|
| FLOAT            |        |                          |               |
| DOUBLE PRECISION |        |                          |               |
| NUMERIC          |        |                          |               |
| DECIMAL          |        |                          |               |


## Date types

| Name      | Size   | Range                    | Description   |
|-----------|--------|--------------------------|---------------|
| DATE      | 64bits | 01/01/0100 - 02/29/32768 | Only date     |
| TIME      | 64bits | 0:00 AM - 23:59.9999 PM  | Only Time     |
| TIMESTAMP | 64bits | 0:00 AM - 23:59.9999 PM  | Date and Time |

*In dialect 1 DATE includes time information*

## Blob Types

| SUBTYPE | Size      | Description                               |
|---------|-----------|-------------------------------------------|
| 0       | Variable  | Binary data (image, video, audio, ...)    |
| 1       | Variable  | Text                                      |
| 2       | Variable  | Internal. Used for firebird to structures |