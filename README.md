# Move kubernetes workload between clusters.

Configure source kubeconfig context. 

Run ``` kubectl proxy ```

Configure target kubeconfig context. 

Run ``` kubectl proxy --port 8011```

Set namespaces to copy in index.ts

Run the script.

(At this moment, namespace needs to be created before.)