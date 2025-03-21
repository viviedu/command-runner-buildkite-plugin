# command-runner-buildkite-plugin

This plugin will enable you to run a command in the plugin steps, which by default run before your command steps.

This is especially useful if subsequent plugins rely on needing to run some command. In our case, as an example, this was checking out only specific submodules before running our docker-compose plugin.

**Plugin ID:** command-runner

## Using the plugin

```yaml
steps:
  - label: "My pipeline step"
    plugins:
      - https://github.com/viviedu/command-runner-buildkite-plugin.git:
          command: "./my-command.sh"
```
