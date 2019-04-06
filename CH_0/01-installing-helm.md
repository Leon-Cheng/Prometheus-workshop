## Installing Helm



### Install the Helm CLI 

check https://github.com/kubernetes/helm/blob/master/docs/install.md for installation

or just

```
curl https://raw.githubusercontent.com/kubernetes/helm/master/scripts/get | bash
```



### Create tiller ServiceAccount and ClusterRoleBinding

```
$ kubectl apply -f https://gist.githubusercontent.com/owensengoku/34807aa5a682abb9d7f4fab3c4ebcb51/raw/378b8823830f86969b8fab0f4aad36e34afeca40/helm-service-account.yaml
```



### Initialize the Helm

```
$ helm init --service-account tiller --upgrade
$HELM_HOME has been configured at ~/.helm.

Tiller (the Helm server-side component) has been upgraded to the current version.
Happy Helming!

```
