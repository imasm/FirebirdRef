# ALTER TABLE

## Alter columns

### Add column
```SQL
ALTER TABLE table ADD column datatype;
```

### Drop column
```SQL
ALTER TABLE table DROP column;
```

### Rename column
```SQL
ALTER TABLE table ALTER old_column_name TO new_column_name;
```

### Multiple commands
```SQL
ALTER TABLE table
    ADD column1 datatype,
    DROP column2;
```
