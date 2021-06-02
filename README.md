# IISConfiguration

The configuration file archive for some special Aiursoft IIS projects

## How to use

Typically, this project is not for you to use. It is only for achieving the `web.config` file from Aiursoft.

But you can learn and get some experience from us.

For example:

### IIS HSTS Configuration

```xml
    <httpProtocol>
     <customHeaders>
        <add name="strict-transport-security" value="max-age=15552001; includeSubDomains; preload" />
     </customHeaders>
    </httpProtocol>
```

### IIS Larget Form support

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <location path="." inheritInChildApplications="false">
    <system.webServer>
      <security>
        <requestFiltering>
          <requestLimits maxAllowedContentLength="4294967295"/>
        </requestFiltering>
      </security>
    </system.webServer>
  </location>
  <system.web>
    <httpRuntime maxRequestLength="2147483647"/>
  </system.web>
</configuration>
```

### IIS double excaping support

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <location path="." inheritInChildApplications="false">
    <system.webServer>
      <security>
        <requestFiltering allowDoubleEscaping="true"/>
      </security>
    </system.webServer>
  </location>
</configuration>
```

## How to contribute

Submit a pull request or create an issue. I will update the production configuration files manually ASAP.