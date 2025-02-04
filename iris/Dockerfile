ARG IMAGE=intersystemsdc/iris-community:2020.3.0.221.0-zpm

# Utilisation de l'image définie précédemment
FROM $IMAGE

# Définition du répertoire de travail
WORKDIR /home/irisowner/dev

# Exécution des étapes nécessaires
RUN --mount=type=bind,src=.,dst=. \
    iris start IRIS && \
    iris session IRIS < iris.script && \
    iris stop IRIS quietly
