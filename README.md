git clone https://github.com/hogehoge789/gcp_terraform-gke-create.git  
docker run -i -t -v $(pwd):/app/ -w /app/ hashicorp/terraform:light init  
docker run -i -t -v $(pwd):/app/ -w /app/ hashicorp/terraform:light plan  
docker run -i -t -v $(pwd):/app/ -w /app/ hashicorp/terraform:light apply  
docker run --rm -v %CD%:/app/ -w /app/ hashicorp/terraform:light destroy -force
