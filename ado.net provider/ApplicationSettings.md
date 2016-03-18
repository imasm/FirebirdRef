# Application Settings

## Configure App.Config

### Define provider
```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>    
    
    <system.data>
        <DbProviderFactories>
            <remove invariant="FirebirdSql.Data.FirebirdClient" />
            <add name="FirebirdClient Data Provider" 
                invariant="FirebirdSql.Data.FirebirdClient"
                description=".Net Framework Data Provider for Firebird"
                type="FirebirdSql.Data.FirebirdClient.FirebirdClientFactory, FirebirdSql.Data.FirebirdClient, Version=4.1.5.0, Culture=neutral, PublicKeyToken=3750abcc3150b00c" />
        </DbProviderFactories>
    </system.data>

</configuration>
```

### Add ConnectionString

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>    
    
    <connectionStrings>
        <add name="DBNAME"
            providerName="FirebirdSql.Data.FirebirdClient"
            connectionString="initial catalog=localhost:dbalias;user id=SYSDBA;password=masterkey;character set=UTF8;dialect=3;" />
    </connectionStrings>

</configuration>
```

### Configure listeners
```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>    
    
    <system.diagnostics>
        <sources>
            <source name="FirebirdSql.Data.FirebirdClient">
               <listeners>
                   <clear />
                    <!-- output to console -->
                   <add name="console" type="System.Diagnostics.ConsoleTraceListener"/>
                </listeners>
            </source>
        </sources>
    </system.diagnostics>

</configuration>
```