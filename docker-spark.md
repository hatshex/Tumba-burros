# Docker spark uninodo

1) Ir al repositorio:
https://github.com/jupyter/docker-stacks/tree/master/all-spark-notebook

2) Instala Jupyter, Spark con R y PySpark
docker pull jupyter/all-spark-notebook 

3) Ejecutar el repo 
sudo  docker run -it --rm -p 8888:8888 -v /hatshex/proyectos:/home/jovyan/work --name spark jupyter/all-spark-notebook

  + it, modo interactivo
  + rm, la imagen se elimina cuando se detiene.
  + name, si no quieres eliminar la imagen, no le pones rm y le agregas un nombre.
  + p ####:####, puerto del contenedor y de la computadora
  + v dirrepo:dircarpeta,volumen asignado con una carpeta de tu computadora

4) Si necesitamos instalar algunos paquetes, hay que entrar al contenedor
  + sudo docker exec -it spark /bin/bash
    - pip install nltk
    - python -m nltk.downloader stopwords
    - python -m nltk.downloader punkt 
