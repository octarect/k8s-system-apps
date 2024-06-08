# k8s-system-apps

## Usage

Copy an example of kustomization.yaml and edit it.

```bash
OVERLAY_NAME=k3s
cp -r manifests/overlays/example manifests/overlays/$OVERLAY_NAME
$EDITOR manifests/overlays/$OVERLAY_NAME
```

Apply manifests to your cluster:

```bash
kustomize build manifests/overlays/$OVERLAY_NAME | kubectl apply -f -
```
