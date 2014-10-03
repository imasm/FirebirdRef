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

## Primary Key

### Add primary key
```SQL
ALTER TABLE SDVZUT ADD PRIMARY KEY (column);
```
Set primary key name
```SQL
ALTER TABLE table ADD CONSTRAINT primaryKeyName PRIMARY KEY (column);
```

### Delete primary key
```SQL
ALTER TABLE table DROP CONSTRAINT primaryKeyName;
```

### Multiple commands
```SQL
ALTER TABLE table
    ADD column1 datatype,
    DROP column2;
```
