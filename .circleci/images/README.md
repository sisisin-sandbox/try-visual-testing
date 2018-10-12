## How to build and release Docker image

```console
TIMESTAMP=$(TZ=JST-9 date "+%Y%m%d-%H%M%S")
echo $TIMESTAMP
IMAGE_ID=sisisin/try-vt-ci:$TIMESTAMP
docker build -t $IMAGE_ID .
docker login
docker push $IMAGE_ID
```
