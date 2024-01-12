# Starting the system

## Start confluent kafka cluster

```bash
helm install local-confluent-kafka helm/cp-helm-charts --version 0.6.0
```

## Start postrges

```bash
kubectl apply -f postgres.yaml
```

## Start food-ordering-system
```bash
kubectl apply -f food-ordering-system.yaml
```

# Stopping

## Stop food-ordering-system
```bash
kubectl delete -f food-ordering-system.yaml
```

## Stop postrges

```bash
kubectl delete -f postgres.yaml
```

## Stop confluent kafka cluster

```bash
helm uninstall local-confluent-kafka
```