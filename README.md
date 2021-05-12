# inventoryplugins


This repo is for example inventory plugins:

Steps you will need to leverage inventory plugins:

Create a repo like this with the following structure:


<pre class="line-number language-yaml"><code>├── collections
│   └── requirements.yml       # Where you put the collections required for plugin
└── now.yml                    # Example of servicenow plugin config
└── foo.yml                    # Where plugin configs go
</code></pre>

When leveraging this in Ansible Automation Platform you will need to create custom credientals to send in the access variables to the plugin.

NOTE: because plugin inventories can connect different ways or need different information this is specific to the plugin/collection used I will provide examples of different ones



WORK IN PROGRESS

