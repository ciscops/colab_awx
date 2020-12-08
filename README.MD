# COLAB AWX
This repo contains an ansible playbook for the COLAB AWX server

## Installation
Install awx collection

    ansible-galaxy collection install awx.awx

Configure appropriate environment variables

    export TOWER_USERNAME=
    export TOWER_PASSWORD=
    export TOWER_HOST=
    export cml_account=
    export cml_password=
    export AWS_ACCESS_KEY_ID=
    export AWS_SECRET_ACCESS_KEY=
    export aws_iam_group=
    export colabot_dev_wxt=
    export colabot_prod_wxt=
    export vcenter_admin_account=
    export vcenter_admin_password=
    export vcenter_sso_group=
    export meraki_auth_vault=
    export meraki_netid_vault=
    export colabot_email=
    export colabot_username=
    export colabot_password=
    export login_server_hostname=
    export login_server_username=
    export login_server_password=

Copy appropriate kubeconfig.yaml file to ./kubeconfig.yaml


Run playbook

    ansible-playbook configure_awx.yaml

In AWX Web Console, click users, click COLABOT, click Permissions, click add permissions, click job templates, 
select all jobs appropriate for COLABOT, give Execute role, and SAVE.
