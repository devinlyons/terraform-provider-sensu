# sensu_role

Get information about a Sensu Role.

For full documentation on Sensu Roles, see [here](https://docs.sensu.io/sensu-go/latest/operations/control-access/rbac/#roles).

## Basic Example

```hcl
data "sensu_role" "role_1" {
  name = "my_role"
}
```

## Argument Reference

* `name` - *Required* - The name of the Sensu role.

* `namespace` - *Optional* - The namespace to manage resources in. This can
  also be set with the `SENSU_NAMESPACE` environment variable. If not set,
  this defaults to `default`.

## Attribute Reference

* `rule` - *Required* - See the [Sensu rbac reference](https://docs.sensu.io/sensu-go/latest/operations/control-access/rbac/#role-and-cluster-role-specification).

### rule

The `rule` block supports:

* `verbs` - *Required* - See the [Sensu rbac reference](https://docs.sensu.io/sensu-go/latest/operations/control-access/rbac/#rules-attributes).

* `resources` - *Required* - See the [Sensu rbac reference](https://docs.sensu.io/sensu-go/latest/operations/control-access/rbac/#rules-attributes).

* `resource_names` - *Optional* - See the [Sensu rbac reference](https://docs.sensu.io/sensu-go/latest/operations/control-access/rbac/#rules-attributes).
