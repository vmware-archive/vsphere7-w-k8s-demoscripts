# Workload Cluster

![](.././images/tkg.png)

To store the Guest Cluster Images we will need to create a Content Library.

1. Navigate to Menu -> Content Libraries -> Create
2. Set name as Kubernetes (case sensitive)
3. Choose Subscribed Content Library and enter in https://wp-content.vmware.com/v2/beta/lib.json for the URL, and choose when needed
![](.././images/contentlibrary.png)

4. Click Yes to accept the certificate thumbprint.
![](.././images/contentlibrary2.png)

![](.././images/contentlibrary3.png)

5. Choose a datastore to store your images.
6. Click Finish

## Create Workload Cluster

Login as admin.

kubectl vsphere login --insecure-skip-tls-verify --server your-wcp-server -u administrator@vsphere.local

Username: administrator@vsphere.local
PW: VMware1!

Switch to the namespace we created.
kubectl config use-context <namespace>

Make sure to use the correct Storage Class that you created and Namespace in the manifest file.

![](.././images/workloadcluster1.png)

kubectl apply -f scripts/create-managed-cluster.yaml

SOMETIMES THE GUEST CLUSTER DOES NOT SHOW UP IN THE VSPHERE UI. 
YOU MAY HAVE TO DELETE AND DO IT AGAIN.

kubectl config use-context guestcluster