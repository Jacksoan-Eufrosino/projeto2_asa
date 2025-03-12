# Projeto 2 de Administração de sistemas abertos

Este projeto demonstra a integração do Vagrant, Ansible e Docker para configurar e gerenciar ambientes de desenvolvimento e produção de forma automatizada. O projeto tem conta com 3 containers:
Container 1 - webproxy usando uma imagem customizada do nginx
Container 2 - webserver usando uma imagem do cms Wordpress
Container 3 - database usando uma imagem do mysql

## Estrutura do Projeto

A estrutura do projeto é composta pelos seguintes arquivos:

- **Vagrantfile**: Define a configuração da máquina virtual Vagrant.
- **docker-compose.yml**: Configura os serviços Docker que serão executados.
- **playbook.yml**: Contém as instruções do Ansible para provisionar a máquina virtual.

## Pré-requisitos

Certifique-se de ter as seguintes ferramentas instaladas em sua máquina host:

- [Vagrant](https://www.vagrantup.com/)
- [VirtualBox](https://www.virtualbox.org/)
- [Ansible](https://www.ansible.com/)

## Passo a Passo para Execução

1. **Clone o repositório:**

   ```bash
   git clone https://github.com/Jacksoan-Eufrosino/projeto2_asa.git
   cd projeto2_asa
   ```

2. **Inicie a máquina virtual com Vagrant:**

   ```bash
   vagrant up
   ```

   Este comando criará e configurará a máquina virtual conforme definido no `Vagrantfile`. Em seguida o Ansible se encarregará de provisionar a máquina virtual com as dependências necessárias como `Docker` e `Docker-Compose`.

3. **Acesse os serviços:**

   Os serviços Docker agora estão em execução, e pagina inicial do wordpress pode ser acessada no endereço `http://192.168.57.10:8080`
