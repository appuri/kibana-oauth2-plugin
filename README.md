# Kibana Auth Plugin
An OAuth Plugin for Kibana 4.  It uses [Bell](https://github.com/hapijs/bell) for the OAuth handling.

### Requirements
Kibana 4.4+

### Installation steps
1. Download and unpack [Kibana](https://www.elastic.co/downloads/kibana).
2. From the Kibana root directory, install the plugin with the following command:

```
bin/kibana plugin -i oauth2 -u https://github.com/appuri/kibana-oauth2-plugin/releases/download/0.3.0/kibana-oauth2-plugin-0.3.0.zip
```

3. Set the following required config options that map to [Bell `server.auth.strategy` options](https://github.com/hapijs/bell/blob/master/API.md):
```
oauth2.password
oauth2.provider
oauth2.clientId
oauth2.clientSecret
```

Optional settings are below

```
oauth2.redirectUri - Used to set `redirect_uri` on `server.auth.strategy.location` manually.
oauth2.forceHttps - Maps to `server.auth.strategy.forceHttps` to infer the `redirect_uri` but use HTTPS as the scheme.
oauth2.allowedOrganizations - Array containing the organizations whose users are allowed to access Kibana.
```

To get the list of supported providers, see [Bell's documentation](https://github.com/hapijs/bell)
