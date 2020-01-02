# petspringdocker
#command to create and install the file
oc create new-project dockerspringpetclinic
oc new-app -e OPENSHIFT_ENABLE_OAUTH=true -e VOLUME_CAPACITY=2Gi jenkins-persistent
oc new-app https://github.com/satishchennu1/petspringdocker.git --strategy=docker --name=petspringdocker
