# How To Do Vulnerability Scanning In K8s With Kube-Hunter :

### Prerequisite :
You should have a Kubernetes cluster running in your machine
Make sure you have python 3 and pip installed

### Installing Kube-Hunter
There are various ways through which you can install the Kube-hunter

You can install it through pip

Secondly, you can also install and use it as a docker container. It will do the scanning from outside the cluster.

Thirdly you can run this as a pod and use it to scan your cluster for Vulnerabilities. Through this method we can do the scanning from inside the cluster.

Lastly, you can directly download and install the latest binary

### To Install Kube-Hunter onto your machine run this command
'''
 pip install --user kube-hunter  

'''
Let’s check what options do we get through this tool

'''
kube-hunter --help

'''
So to check what all tests we can perform with Kube-hunter run this list command, and it will list all the test.

'''
Kube-hunter --list

'''

### Scanning The Cluster :
Let’s Start doing the scans , For this you can run this command

'''
kube-hunter 

'''
### In your terminal which will give you the list of nodes in your cluster along with Their IP
'''
kubectl get nodes -o wide

'''

### Testing this tool on a Multi-Node Cluster
To test this, I created a multi-node cluster with 2 worker nodes and 1 master and on this, we will be doing the vulnerability scanning.

suppose it we want to get the JSON format of Scanning

'''
kube-hunter --remote 172.19.0.6 -- report json

'''

I hope it is easy to understand, now let’s apply this manifest through this command

'''
kubectl apply -f filename

'''
Now you can check the list of pods to see if it is running or not
'''
kubectl get pods

'''



