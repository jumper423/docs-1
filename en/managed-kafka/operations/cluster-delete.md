---
title: "Deleting Apache Kafka clusters"
description: "You can delete an Apache Kafka® cluster if you no longer need it. All data in the cluster will be deleted. In the management console, select the directory from which you want to delete the cluster."
---

# Deleting a cluster

You can delete an {{ KF }} cluster if you no longer need it. All data in the cluster will be deleted.

{% list tabs %}

- Management console

  1. In the [management console]({{ link-console-main }}), select the folder to delete the cluster from.
  1. Select **{{ mkf-name }}**.
  1. Click ![image](../../_assets/options.svg) for the cluster and select **Delete cluster**.
  1. Read the warning displayed. Confirm cluster deletion and click **Delete**.

- CLI

  {% include [cli-install](../../_includes/cli-install.md) %}

  {% include [default-catalogue](../../_includes/default-catalogue.md) %}

  To delete a cluster, run the command:

  ```
  {{ yc-mdb-kf }} cluster delete <cluster name or ID>
  ```

- Terraform

  {% include [terraform-delete-mdb-cluster](../../_includes/mdb/terraform-delete-mdb-cluster.md) %}


- API

  To delete a cluster, use the [delete](../api-ref/Cluster/delete.md) API method: pass the cluster ID in the `clusterId` request parameter.

  To find out the cluster ID, [get a list of clusters in the folder](cluster-list.md#list-clusters).

{% endlist %}

