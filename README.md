# command-runner-buildkite-plugin

This plugin will enable you to run a command in any of the plugin steps.

This is especially useful if you want to customise your checkout. In our case, as an example, this was checking out only specific submodules for our docker-compose plugin.

## Using the plugin

```yaml
steps:
  - label: "My pipeline step"
    plugins:
      - https://github.com/viviedu/command-runner-buildkite-plugin.git#master:
          precheckout: "./my-pre-checkout-script.sh"
          checkout: "./my-checkout-script.sh"
          postcheckout: "./my-postcheckout-script.sh"
```
