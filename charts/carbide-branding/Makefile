install-local:
	helm upgrade --install docs  -n carbide-system  --create-namespace .
delete:
	helm delete -n carbide-system docs
build:
	helm package carbide-branding
push:
	helm push carbide-carbide-branding-0.1.0.tgz oci://harbor.lark.lol/public/carbide-carbide-branding
