# 📜 vagrant
Criação de máquinas virtuais

### Descrição: 
Utilize esse projeto para criar três máquinas virtuais, utilizando o VirtualBox. Assim, rapidamente você terá um ambiente de desenvolvimento para os seus estudos de Docker ou Kubernetes, por exemplo.

### Pré-requisitos 
 - Instalação do [Virtual box](https://www.virtualbox.org/)
 - Instalação do [Vagrant](https://www.vagrantup.com/)


### 📘 Tabela de comandos 

|COMANDO| DESCRIÇÃO
|------|------
|vagrant init| Inicializa e cria o arquivo vagrantfile
|vagrant up| Inicialização as máquinas virtuais
|vagrant halt| Desliga as máquinas virtuais
|vagrant ssh <maq.virtual>| Acessa a máquina virtual
|vagrant box list| Exibe as lista de imagens


### 🖥️ Execução do projeto
Após a instalação do VirtualBox e do Vagrant, digite o comando "*vagrant ini*". Em seguida, substitua o arquivo vagrantfile por esse do repositório. Em seguida execute o comando "*vagrant up*". Para acessar uma das máquinas recém criadas, digite o comando "*vagrant ssh <nome_vm>*".

```c
vagrant init
  
vagrant up

vagrant ssh <nome_vm>

vagrant halt
```

Caso queira instalar algum programa durante a criação da máquina virtual, adicione o trecho abaixo, no arquivo vagrantfile:

```c
config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y apache2
    service apache2 start
  SHELL
end
```