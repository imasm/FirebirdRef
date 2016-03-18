## Create database

## Create database programatically

```csharp
static void CreateFBDatabase()
{
    int pageSize = 4096;
    bool forcedWrites = false;
    bool overwrite = true;

	FbConnectionStringBuilder csb = new FbConnectionStringBuilder();
	csb.Database = 'dbFilename';
	csb.DataSource = 'dbhost';
	csb.UserID = 'user';
	csb.Password = 'password';
    csb.Dialect = 3;
    csb.Charset = 'UTF8'

	FbConnection.CreateDatabase(csb.ConnectionString, pageSize, forcedWrites, overwrite);
}
```