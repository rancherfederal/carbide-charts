install-local:
	helm upgrade --install docs  -n carbide-system  --create-namespace .
delete:
	helm delete -n carbide-system docs
build:
	helm package offline-docs
push:
	helm push carbide-offline-docs-0.1.0.tgz oci://harbor.lark.lol/public/carbide-offline-docs