Para actualizar el Secret necesario para importa las imágenes desde la registry del cluster NO-PROD, al cluster PROD, debe ejecutarse:
- oc delete -f desa-copy-image-secret.yaml (para borrar el secret definido en el template)
- oc create -f desa-copy-image-secret.yaml

Para actualizar el Secret necesario para acceder al repositorio de las apps (GitLab):
- oc delete -f repository-credentials.yaml (para borrar el secret definido en el template)
- oc create -f repository-credentials.yaml