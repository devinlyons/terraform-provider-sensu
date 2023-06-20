# sensu_hook

Manages a Sensu Hook.

For full documentation on Sensu Hooks, see [here](https://docs.sensu.io/sensu-go/latest/observability-pipeline/observe-schedule/hooks/).

## Basic Example

```hcl
resource "sensu_hook" "hook_1" {
  name = "my_hook"
  command = "/usr/local/bin/foo"
}
```

## Argument Reference

* `name` - *Required* - The name of the Sensu hook.

* `namespace` - *Optional* - The namespace to manage resources in. This can
  also be set with the `SENSU_NAMESPACE` environment variable. If not set,
  this defaults to `default`.

* `command` - *Required* - See the [Sensu hook reference](https://docs.sensu.io/sensu-go/latest/observability-pipeline/observe-schedule/hooks/#hook-specification).

* `timeout` - *Optional* - See the [Sensu hook reference](https://docs.sensu.io/sensu-go/latest/observability-pipeline/observe-schedule/hooks/#hook-specification).
  Defaults to 60.

* `stdin` - *Optional* - See the [Sensu hook reference](https://docs.sensu.io/sensu-go/latest/observability-pipeline/observe-schedule/hooks/#hook-specification).
  Defaults to false.

## Attribute Reference

The resource has no computed fields.
