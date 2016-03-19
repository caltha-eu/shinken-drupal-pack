# Drupal monitoring configuration pack for Shinken

You Drupal site needs to have https://www.drupal.org/project/nagios installed and configured.

Just put this configuration in your Shinken configuration directory (like /etc/shinken/packs/drupal) and apply configuration to your host as in example below. Don't forget to restart/reload Shinken.


```
define host {
   use             generic-host,drupal
   host_name       <your host name>
   address         <your host address>

   #Drupal params
   _UNIQUE_ID      <your Drupal Nagios module Unique ID
   _NAGIOS_PATH    <path to your nagios monitoring page>
   _TIMEOUT        <timeout>
}
```

Happy monitoring!
