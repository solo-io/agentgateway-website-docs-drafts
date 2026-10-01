{{< reuse "agw-docs/snippets/review-table.md" >}} For more information, see the [Helm reference docs]({{< link-hextra path="/reference/helm/" >}}).

| Value | Use |
| --- | --- |
| `replicaCount` | Run more than one proxy pod. |{{< version exclude-if="1.5.x" >}}
| `autoscaling` | Create a HorizontalPodAutoscaler for the proxy Deployment. For an example, see [Scale with a HorizontalPodAutoscaler](#standalone-helm-hpa). |{{< /version >}}
| `monitoring.enabled` | Create a PodMonitor and expose the metrics port for Prometheus Operator. |
| `extraEnv`, `extraVolumes`, `extraVolumeMounts`, `extraContainers` | Add environment variables, mount secrets, or run sidecars. |
| `imagePullSecrets` | Pull the proxy image from a private registry. |
| `image.registry`, `image.repository`, `image.tag` | Pull the proxy image from another registry, such as an internal mirror. |
