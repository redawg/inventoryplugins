# inventoryplugins


This repo is an example of how to setup inventory plugins with AAP (Controller/Tower):

Steps you will need to leverage inventory plugins:

Create a repo like this with the following structure:

<pre class="line-number language-yaml"><code>├── collections
│   └── requirements.yml       # Where you put the collections required for plugin
└── now.yml                    # Example of servicenow plugin config
└── foo.yml                    # Where plugin configs go
</code></pre>

When leveraging this in Ansible Automation Platform you will need to create custom credientals to send in the access variables to the plugin.

NOTE: because plugin inventories can connect different ways or need different information this is specific to the plugin/collection used I will provide examples of different ones


<B>CREATE A NEW PROJECT FOR INVENTORY PLUGINS:</B>
![image](https://user-images.githubusercontent.com/17077661/118025735-04bb4900-b315-11eb-88e5-27a3afee8ccc.png)

Create Custom Creds - Example Service NOW ITSM

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
![image](https://user-images.githubusercontent.com/17077661/118027549-e9e9d400-b316-11eb-903a-a9131e218eac.png)
NOW Create new Creds using the custom creds just created - Note the Creds created above are built to be used by this plugin and playbooks that need credentials to update tickets etc. 
![image](https://user-images.githubusercontent.com/17077661/118028290-c5422c00-b317-11eb-8908-fd66352ae226.png)


<B2>CREATE A NEW INVENTORY</B2>
![image](https://user-images.githubusercontent.com/17077661/118025859-24527180-b315-11eb-840a-4ca83e530006.png)

<B> ADD A SOURCE TO THE INVENTORY </B>
![image](https://user-images.githubusercontent.com/17077661/118025958-2d434300-b315-11eb-97d1-02cf21897d8e.png)

<B EDIT SOURCE DETAILS WITH CREATED CREDS, PROJECT, and INVENTORY FILE (how you want to parse)
![image](https://user-images.githubusercontent.com/17077661/118028880-721ca900-b318-11eb-985a-46b39f079a6a.png)









WORK IN PROGRESS

