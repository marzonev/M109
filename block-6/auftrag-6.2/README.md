# Auftrag 6.2: HTML-Seite auf OpenShift deployen

## Deployment

Deployment ist für die Aufsetzung des Containers

```k8s
kind: Deployment
apiVersion: apps/v1
metadata:
  name: html-openshift-app
  labels:
    app: html-openshift-app
    app.kubernetes.io/part-of: html-openshift-app
spec:
  replicas: 1
  selector:
    matchLabels:
      app: html-openshift-app
  template:
    metadata:
      labels:
        app: html-openshift-app
    spec:
      containers:
      - name: html-openshift-app
        resources: {}
        ports:
        - containerPort: 8080
          protocol: TCP
        image: ghcr.io/<Github-Username>/html-openshift-app:v1
        imagePullPolicy: Always
```

[Deployment-file](oc/deployment.yaml)

## Service

Service ist für die Netzwerkkonfiguration im Cluster.

```k8s
kind: Service
apiVersion: v1
metadata:
  name: html-openshift-app
  labels:
    app: html-openshift-app
    app.kubernetes.io/part-of: html-openshift-app
spec:
  ports:
    - name: http
      protocol: TCP
      port: 8080
      targetPort: 8080
  selector:
    app: html-openshift-app
```

[Service-file](oc/service.yaml)

## Route

Route ist für die Netzwerkkonfiguration für externen Zugriff auf den Container.

Das ist von Openshift und ist nicht im Standart Kubernetes. Das sieht man, da bei der apiVersion eine openshift api verwendet wird.

```
kind: Route
apiVersion: route.openshift.io/v1
metadata:
  name: html-openshift-app
  labels:
    app: html-openshift-app
    app.kubernetes.io/part-of: html-openshift-app
spec:
  to:
    kind: Service
    name: html-openshift-app
  port:
    targetPort: http
  tls:
    termination: edge
    insecureEdgeTerminationPolicy: Redirect
```

[Route-file](oc/route.yaml)