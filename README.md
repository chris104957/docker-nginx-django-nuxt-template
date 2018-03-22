# docker-nginx-django-nuxt-template
This repository provides a template for deploying a Django backend served by Nginx/Gunicorn on port 8000, and a NuxtJS/Vuetify front end served by Node on port 80

Prerequisites
---
1. Docker: https://docs.docker.com/install/#supported-platforms
2. docker-compose: https://docs.docker.com/compose/install/
3. An AWS account

Instructions
---
In an empty directory:
1. Create docker machine (replace ``MY_AWS_ACCESS_KEY``, ``MY_SECRET_KEY`` and ``machine_name`` as appropriate)
```
docker-machine create -d amazonec2 --amazonec2-access-key MY_AWS_ACCESS_KEY --amazonec2-secret-key MY_SECRET_KEY machine_name
```

2. Setup the environment
```
docker-machine env machine_name
```

3. Clone this repository (or your own fork) and cd into it
```
git clone https://github.com/chris104957/docker-nginx-django-nuxt-template.git && cd docker-nginx-django-nuxt-template
```

4. Build and deploy image
```
docker-compose build
docker-compose up -d
```

5. Go to the AWS console and look in your EC2 **running instances** for the machine, open port 80, then go to the public IP to see if it worked
