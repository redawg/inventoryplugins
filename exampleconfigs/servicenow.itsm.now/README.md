<B>Create Custom Creds - Example Service NOW ITSM </B>

INPUT CONFIGURATION:
<pre class="line-number language-yaml"><code>fields:
  - id: username
    type: string
    label: Username
  - id: password
    type: string
    label: Password
    secret: true
  - id: instance
    type: string
    label: Short Hostname (instance)
  - id: host
    type: string
    label: FQDN Instance URL
</code></pre>
INJECTOR CONFIGURATION:
<pre class="line-number language-yaml"><code>env:
  SN_HOST: '{{host}}'
  SN_INSTANCE: '{{instance}}'
  SN_PASSWORD: '{{password}}'
  SN_USERNAME: '{{username}}'
extra_vars:
  SN_HOST: '{{host}}'
  SN_INSTANCE: '{{instance}}'
  SN_PASSWORD: '{{password}}'
  SN_USERNAME: '{{username}}'
</code></pre>
