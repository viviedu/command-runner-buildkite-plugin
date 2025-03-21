# command-runner-buildkite-plugin

This plugin will enable you to run a command in any of the plugin checkout steps.

## Using the plugin

```yaml
steps:
  - label: "My pipeline step"
    plugins:
      - https://github.com/viviedu/custom-checkout-buildkite-plugin.git#master:
          precheckout: "./my-pre-checkout-script.sh"
          checkout: "./my-checkout-script.sh"
          postcheckout: "./my-postcheckout-script.sh"
```
