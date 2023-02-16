cd ~/.kube

shahzhas@SHAHZHAS-M-F7DG .kube % kubectl config get-contexts
CURRENT   NAME             CLUSTER          AUTHINFO         NAMESPACE
          docker-desktop   docker-desktop   docker-desktop   
*         minikube         minikube         minikube         default


aws eks update-kubeconfig --name <cluster_name> --region us-west-2
  - by doing this we can get the aws context for given cluster_name

oc login https://api.xyz.pqr.io:<port_number>/ -u kubeadmin -p qGuxc-oRz6n-hLVK3-KHaaa

brew install openshift-cli

shahzhas@SHAHZHAS-M-F7DG .kube % oc login https://api.xyz.pqr.io:<port_number>/ -u kubeadmin -p qGuxc-oRz6n-hLVK3-KHaaa

Login successful.
You have access to 74 projects, the list has been suppressed. You can list all projects with 'oc projects'

shahzhas@SHAHZHAS-M-F7DG .kube % kubectl config get-contexts                                                                 
CURRENT   NAME                                                    CLUSTER                              AUTHINFO                                        NAMESPACE
*         default/api.xyz.pqr.io:<port_number>/kube:admin   api.xyz.pqr.io:<port_number>   kube:admin/api.xyz.pqr.io:<port_number>                     default
          docker-desktop                                          docker-desktop                       docker-desktop                                  
          minikube                                                minikube                             minikube                                        default

kubectl get ns 
  - This will give namespaces of current context , in above case api.xyz.pqr.io cluster

shahzhas@SHAHZHAS-M-F7DG .kube % 
shahzhas@SHAHZHAS-M-F7DG .kube % kubectl config use-context minikube
Switched to context "minikube".
shahzhas@SHAHZHAS-M-F7DG .kube % 
shahzhas@SHAHZHAS-M-F7DG .kube % kubectl config get-contexts        
CURRENT   NAME                                                    CLUSTER                              AUTHINFO                                        NAMESPACE
          default/api.xyz.pqr.io:<port_number>/kube:admin   api.xyz.pqr.io:<port_number>   kube:admin/api.xyz.pqr.io:<port_number>                     default
          docker-desktop                                          docker-desktop                       docker-desktop                                  
*         minikube                                                minikube                             minikube                                        default

kubectl get ns 
  - This will give namespaces of current context , in above case minikube cluster


