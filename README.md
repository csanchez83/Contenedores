# Contenedores
Pasos para Implementar un Contenedor en Docker y posterior subirlo a Azure App Services

#Utilizando una Virtual Machine de Azure con Linux, instala Docker con los siguientes pasos:

# Instalacion Docker en Ubuntu 22.04

# Configurando el repositorio
    sudo apt update
    sudo apt install ca-certificates curl gnupg -y
  
# Agregar las llaves GPG oficiales de Docker
    sudo mkdir -m 0755 -p /etc/apt/keyrings
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
  
# Agregar el repo
    echo \
    "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
    "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
    sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  
# Instalacion Final
    sudo apt update
    sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
    
    
# Hello World
    sudo docker run hello-world
