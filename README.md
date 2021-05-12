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


![image](https://user-images.githubusercontent.com/17077661/118025603-e2c1c680-b314-11eb-8673-041edb694487.png)

![image](https://user-images.githubusercontent.com/17077661/118025735-04bb4900-b315-11eb-88e5-27a3afee8ccc.png)

![image](https://user-images.githubusercontent.com/17077661/118025859-24527180-b315-11eb-840a-4ca83e530006.png)

![image](https://user-images.githubusercontent.com/17077661/118025958-2d434300-b315-11eb-97d1-02cf21897d8e.png)

![image](https://user-images.githubusercontent.com/17077661/118026151-5cf24b00-b315-11eb-8805-64c7f6c9babe.png)





WORK IN PROGRESS

