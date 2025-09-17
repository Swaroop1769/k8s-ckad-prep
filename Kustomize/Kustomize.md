## Problem

- We want to reuse our Kubernetes configs and only modify what needs to be changed on a per-environment basis.
    - what we don't want is - copy all of our configs across each and every environment (not a scalable solution)

- Kustomize has 2 key words
1. base (config that's identical across all environments. And also represents default values across all the environments)
2. Overlays (allows us to customize the behavior on per-environment basis)

- Base + Overlay (with Kustomize) ==> Final Manifests



### Kustomize vs Helm

- Helm makes use of go templates to allow assigning variables to properties



