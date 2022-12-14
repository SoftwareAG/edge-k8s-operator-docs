# Cumulocity IoT Edge Kubernetes Operator User Guide

* **[Overview](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/01-overview)**
* **[Architecture](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/02-architecture)**
* **[Getting Started](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started)**
    * **[System Requirements](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#system-requirements)**
        * **[K3s](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#k3s)**
        * **[K3d](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#k3d)**
    * **[Install Operator](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#install-operator)**
        * **[Requirements](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#requirements)**
        * **[Get Helm Charts](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#get-helm-charts)**
        * **[Deploy Edge Kubernetes Operator](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#deploy-edge-kubernetes-operator)**
    * **[Install Edge](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#install-edge)**
        * **[Requirements](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#requirements)**
        * **[Configure Kubernetes with private registry](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#configure-kubernetes-with-private-registry)**
        * **[Domain Name System (DNS) setup](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#domain-name-system-dns-setup)**
        * **[Create Kubernetes Manifest with Edge Custom Resource (CR)](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#create-kubernetes-manifest-with-edge-custom-resource-cr)**
        * **[Deploy Edge](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#deploy-edge)**
        * **[Verify Edge deployment](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#verify-edge-deployment)**
    * **[Accessing Edge](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#accessing-edge)**
        * **[Configuring access through domain name](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#configuring-access-through-domain-name)**
        * **[Accessing through domain name](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#accessing-through-domain-name)**
    * **[Accessing logs](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#accessing-logs)**
    * **[Troubleshooting](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/03-getting-started#troubleshooting)**
* **[Edge Custom Resource Definition](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition)**
    * **[Configuration](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#configuration)**
    * **[Spec](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#spec)**
    * **[License Secret](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#license-secret)**
    * **[TLS Secret](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#tls-secret)**
    * **[Admin Credentials Secret](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#admin-credentials-secret)**
    * **[Cumulocity IoT Core configurations](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#cumulocity-iot-core-configurations)**
    * **[Cumulocity IoT Core values](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#cumulocity-iot-core-values)**
    * **[Microservices](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#microservices)**
    * **[Applications](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#applications)**
    * **[MongoDb](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#mongodb)**
    * **[MongoDB Credentials Secret](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#mongodb-credentials-secret)**
    * **[Microservices Registry](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#microservices-registry)**
    * **[Microservices Registry Credentials Secret](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#microservices-registry-credentials-secret)**
    * **[Microservices Registry TLS Secret](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#microservices-registry-tls-secret)**
    * **[Resource Limits Spec](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#resource-limits-spec)**
    * **[Software AG Registry Credentials Secret](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/04-edge-custom-resource-definition#software-ag-registry-credentials-secret)**
* **[Management](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/05-manage-edge-deployment)**
    * **[Modify Edge deployment](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/05-manage-edge-deployment#modify-edge-deployment)**
        * **[Example Configuration Change](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/05-manage-edge-deployment#example-configuration-change)**
    * **[Version upgrade](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/05-manage-edge-deployment#version-upgrade)**
        * **[Start the Upgrade](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/05-manage-edge-deployment#start-the-upgrade)**
    * **[Undeploy Edge](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/05-manage-edge-deployment#undeploy-edge)**
* **[Manage Operator](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/06-manage-operator)**
    * **[Upgrade Operator](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/06-manage-operator#upgrade-operator)**
    * **[Undeploy Edge](https://github.com/SoftwareAG/edge-k8s-operator-docs/wiki/06-manage-operator#undeploy-operator)**
    
______________________
These tools are provided as-is and without warranty or support. They do not constitute part of the Software AG product suite. Users are free to use, fork and modify them, subject to the license agreement. While Software AG welcomes contributions, we cannot guarantee to include every contribution in the master project.	
