# command-runner-buildkite-plugin

This plugin will enable you to run a command in any of the plugin checkout steps.

Be cautious with pointing these commands to run any bash scripts or files contained within your repo - these files won't be accessible until you've checked out. The commands must be run inline prior to checkout completion.

If you wish to use this plugin to customise your checkout step, ensure to skip the checkout step of any adjascent plugins to avoid conflicts.

## Using the plugin

```yaml
steps:
  - label: "My pipeline step"
    plugins:
      - https://github.com/viviedu/command-runner-buildkite-plugin.git#master:
          precheckout: echo "preparing my repo" && <any command>
          checkout: git checkout <my repo>
          postcheckout: echo "checked out repo && <any command>
```
