# 📜 vagrant
Criação de máquinas virtuais

### Descrição: 
Utilize esse projeto para criar três máquinas virtuais, utilizando o VirtualBox. Assim, rapidamente você terá um ambiente de desenvolvimento para os seus estudos de Docker, Kubernetes, etc. 

### Pré-requisitos 
 - Instalação do [Virtual box](https://www.virtualbox.org/)
 - Instalação do [Vagrant](https://www.vagrantup.com/)

 - Instalação do [Gitbash](https://git-scm.com/downloads)


### 📘 Tabela de comandos 

|COMANDO| DESCRIÇÃO
|------|------
|vagrant init             | Cria o arquivo vagrantfile
|vagrant up               | Inicializa todas as máquinas virtuais
|vagrant up --provision nome_vm1 nome_vm2 | Provisiona apenas as máquinas virtuais informadas
|vagrant status           | Exibe as máquinas virtuais
|vagrant halt             | Desliga as máquinas virtuais
|vagrant ssh <maq.virtual>| Acessa a máquina virtual
|vagrant box list         | Exibe uma lista de imagens
|vagrant destroy <maq.virtual>| Destrói a máquina virtual

### 🖥️ Execução do projeto
1 - Instale o VirtualBox e o Vagrant em sua máquina desktop.

2 - Faça o clone desse projeto:
```c
git clone https://github.com/robson-devops/vagrant.git

``` 
3 - Acesse o diretório vagrant e execute o comando ``vagrant up``. 
Para acessar uma das máquinas recém criadas, digite o comando ``vagrant ssh <nome_vm>``.

```c
cd vagrant/

vagrant up

vagrant ssh <nome_vm>
```

Para desligar as máquinas virtuais, utilize o comando abaixo: 
```
vagrant halt
```
### ✋ Observação 
Caso queira alterar a imagem que será instalada na VM, acesse o site https://app.vagrantup.com/boxes/search 

Se ocorrer erro na execução do comando ``vagrant up``, desabilite seu antivirus.


<center><h6>robson-devops @2022<h6></center>