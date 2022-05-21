# Detic_docker

# CPU version
cd cpu
docker build -t detic_cpu .


imagesがマウントできるフォルダに移動して、
`
docker run -it -v $PWD/images:/images -v $PWD/cpu/scripts:/scripts detic:test
`