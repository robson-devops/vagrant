# 📜 vagrant
Criação de máquinas virtuais

### Descrição: 
Utilize esse projeto para criar três máquinas virtuais, utilizando o VirtualBox. Assim, rapidamente você terá um ambiente de desenvolvimento para os seus estudos de Docker ou Kubernetes, por exemplo.

### Pré-requisitos 
 - Instalação do [virtual box](https://www.virtualbox.org/)
 - Instalação do [vagrant](https://www.vagrantup.com/)


### 📘 Tabela de comandos 

|COMANDO| DESCRIÇÃO
|------|------
|vagrant init| Inicializa e criar o arquivo vagrantfile
|vagrant up| Iniciali as máquinas virtuais
|vagrant halt| Desliga as máquinas virtuais
|vagrant ssh <maq.virtual>| Acessa a máquina virtual
|vagrant box list| Exibe as lista de imagens


### 🖥️ Execução do projeto
Após a instalação do VirtualBox e do vagrant, digite o comando *vagrant ini*. Em seguida, substitua o arquivo vagrantfile por esse do repositório. Em seguida execute o comando *vagrant up*. Para acessar uma das máquinas recém criadas, digite o comando *vagrant ssh <nome_máquina>*.

```c
vagrant init
  
vagrant up

vagrant ssh <nome_machine>

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