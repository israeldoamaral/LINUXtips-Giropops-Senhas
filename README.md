# LINUXtips-Giropops-Senhas
Repo para a prática do projeto PICK - Programa Intensivo de Docker e Kubernetes 2024.


# Ferramentas Utilizadas

* Docker
* Trivy
* Cosing

## Objetivo
Criar uma imagem segura, eficiente e minimalista utilizando como base o  projeto giropops-senha. Criar recursos de automação e monitoramento.

## Instalação das ferramentas

* Docker 
```
curl -fsSL https://get.docker.com/ | bash
```

* Trivy
```
sudo apt-get install wget apt-transport-https gnupg lsb-release
wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | sudo apt-key add -
echo deb https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main | sudo tee -a /etc/apt/sources.list.d/trivy.list
sudo apt-get update
sudo apt-get install trivy
```

* Cosing
```
curl -O -L "https://github.com/sigstore/cosign/releases/latest/download/cosign-linux-amd64"
sudo mv cosign-linux-amd64 /usr/local/bin/cosign
sudo chmod +x /usr/local/bin/cosign
```


## Iniciando o projeto

### Vamos fazer o fork do repositório que contem a aplicação.

https://github.com/badtuxx/giropops-senhas

## Criação da Imagem
> [!NOTE]
> **Vamos criar a imagem da aplicação 