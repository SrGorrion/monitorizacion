# monitorizacion
pi_monitorizacion

SCRIPT PARA INSTALACIÓN NORMAL:

#!/bin/bash
set -e

echo "Buscando actualizaciones..."
sudo apt update

echo "Instalando Docker y Docker Compose..."
sudo apt install -y docker.io docker-compose

echo "Clonando el proyecto de monitorización..."
git clone https://github.com/SrGorrion/monitorizacion.git
cd monitoring

echo "Levantando los servicios..."
docker-compose up -d

echo "Su sistema de monitorización ha sido instalado con éxito"

__
__

tree:

monitoring
	docker-compose.yml
	grafana
	prometheus
		prometheus.yml
