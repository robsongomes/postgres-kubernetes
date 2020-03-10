# Deploying

Deploying the project is easy with kustomize. The **kustomization.yml** defines the sequence of applying resources. Use the command below to deploy Postgres.

`$ kubectl apply -k .`

If you prefer, you can apply each file individually:

`$ kubectl apply -f postgres-configmap.yml`

# Accessing

After deploying the project, kubernetes will expose the following service:

- postgres on ports:
  - 30432 (external)
  - 5432  (internal)