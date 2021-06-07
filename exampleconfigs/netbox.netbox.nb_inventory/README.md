<B>Create Custom Creds - Example Netbox </B>

INPUT CONFIGURATION:
<pre class="line-number language-yaml"><code>fields:
 - id: netbox_api
   type: string
   label: Netbox API Endpoint
 - id: netbox_token
   type: string
   label: API Token
   secret: true

</code></pre>
INJECTOR CONFIGURATION:
<pre class="line-number language-yaml"><code>env:
  NETBOX_API: '{{netbox_api}}'
  NETBOX_TOKEN: '{{netbox_token}}'
</code></pre>
