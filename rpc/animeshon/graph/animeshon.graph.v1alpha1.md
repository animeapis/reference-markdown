# Package animeshon.graph.v1alpha1

## Index
- [Graph](#animeshon.graph.v1alpha1.Graph)
- [DeleteGraphRequest](#animeshon.graph.v1alpha1.DeleteGraphRequest)
- [MigrateGraphRequest](#animeshon.graph.v1alpha1.MigrateGraphRequest)

## Graph {#animeshon.graph.v1alpha1.Graph}

| MigrateGraph |
| --- |
| **rpc** MigrateGraph([MigrateGraphRequest](#animeshon.graph.v1alpha1.MigrateGraphRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

| DeleteGraph |
| --- |
| **rpc** DeleteGraph([DeleteGraphRequest](#animeshon.graph.v1alpha1.DeleteGraphRequest)) [.google.protobuf.Empty](#google.protobuf.Empty)<br/> |

## DeleteGraphRequest {#animeshon.graph.v1alpha1.DeleteGraphRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the resource to delete. |
## MigrateGraphRequest {#animeshon.graph.v1alpha1.MigrateGraphRequest}

| Field | Description |
| --- | --- |
| name | **[ string](#string)**<br/>The resource name of the resource to migrate. |
