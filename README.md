# ado-terraform
Create an organization in Azure DevOps

Get an access token

Get this project : 

``git clone https://github.com/canatac/ado-terraform.git``

Then intialize the terraform configuration

``terraform init``

Run the planned actions

``terraform plan``

If you agree with

``terraform apply -var project_name="YOUR_PROJECT"``

After that, if you want to clean your workspace : 

``terraform destroy -var project_name="YOUR_PROJECT"``

If you want to run terraform within a docker image : 

PLAN : 

``docker run -i -t -v $PWD:$PWD -w $PWD hashicorp/terraform:1.5.4 plan -var project_name="YOUR_PROJECT"``

APPLY : 

``docker run -i -t -v $PWD:$PWD -w $PWD hashicorp/terraform:1.5.4 apply -var project_name="YOUR_PROJECT"`` 

DESTROY : 

``docker run -i -t -v $PWD:$PWD -w $PWD hashicorp/terraform:1.5.4 destroy -var project_name="YOUR_PROJECT"``