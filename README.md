# service-interconnect-lab-instructions

## Run solution explorer locally

To run the instructions locally execute the following command:

```shell
docker run --rm -it -p 5001:5001 --name solex \
    -v $PWD/walkthroughs:/opt/user-walkthroughs \
    -e NODE_ENV=production \
    -e THREESCALE_WILDCARD_DOMAIN=apps.your-domain.com \
    -e OPENSHIFT_VERSION=4 \
    -e WALKTHROUGH_LOCATIONS='/opt/user-walkthroughs' \
    quay.io/redhatintegration/tutorial-web-app:latest
```