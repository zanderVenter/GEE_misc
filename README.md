# GEE_misc
Google Earth Engine related scripts

# Setting up instance
set "CONTAINER_IMAGE_NAME=gcr.io/earthengine-project/datalab-ee:latest"
set "INSTANCE_NAME=datalab-ee-vm"
datalab create --image-name %CONTAINER_IMAGE_NAME% %INSTANCE_NAME%

# Connecting to instance
datalab connect datalab-ee-vm

# Closing down instance
datalab stop datalab-ee-vm

# Delete data on persistent disk in VM - will delete all data assocaited with instance!
datalab delete --delete-disk datalab-ee-vm
