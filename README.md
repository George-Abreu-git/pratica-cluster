# 🐳 Pratica Cluster — Docker Swarm com Vagrant

Projeto prático de criação de um cluster Docker Swarm utilizando Vagrant e VirtualBox, provisionando automaticamente um nó master e três workers em máquinas virtuais Ubuntu 24.04.

---

## 🧠 Sobre o Projeto

Este projeto tem como objetivo simular um ambiente de cluster real, onde múltiplos nós se comunicam em uma rede privada e são orquestrados pelo Docker Swarm — tudo isso de forma automatizada via Vagrant.

---

## 🏗️ Arquitetura do Cluster

| Nó       | Função  | IP              | Memória | CPU |
|----------|---------|-----------------|---------|-----|
| `master` | Manager | 192.168.56.100  | 1024MB  | 1   |
| `node01` | Worker  | 192.168.56.101  | 1024MB  | 1   |
| `node02` | Worker  | 192.168.56.102  | 1024MB  | 1   |
| `node03` | Worker  | 192.168.56.103  | 1024MB  | 1   |

---

## 📁 Estrutura de Arquivos

```
pratica-cluster/
├── Vagrantfile   # Define e provisiona as VMs do cluster
├── docker.sh     # Instala o Docker em todos os nós
├── master.sh     # Inicializa o Docker Swarm no nó master
└── worker.sh     # Conecta os workers ao Swarm
```

---

## ✅ Pré-requisitos

- [Vagrant](https://www.vagrantup.com/) instalado
- [VirtualBox](https://www.virtualbox.org/) instalado
- Ao menos **4GB de RAM** disponíveis na máquina host

---

## 🚀 Como Executar

Clone o repositório e suba o cluster com um único comando:

```bash
git clone https://github.com/George-Abreu-git/pratica-cluster.git
cd pratica-cluster
vagrant up
```

O Vagrant irá automaticamente:
1. Criar as 4 VMs (master + 3 workers)
2. Instalar o Docker em todas elas
3. Inicializar o Swarm no master
4. Registrar os workers no cluster

---

## 🛠️ Tecnologias Utilizadas

- **Vagrant** — Provisionamento e gerenciamento das VMs
- **VirtualBox** — Hypervisor para execução das máquinas virtuais
- **Docker** — Plataforma de conteinerização
- **Docker Swarm** — Orquestração nativa de containers em cluster
- **Shell Script** — Automação do provisionamento
- **Ubuntu 24.04** — Sistema operacional base das VMs

---

## 📚 O que Aprendi

- Provisionamento automatizado de múltiplas VMs com Vagrant
- Configuração de redes privadas entre nós de um cluster
- Instalação e configuração do Docker via Shell Script
- Inicialização e gerenciamento de um cluster Docker Swarm
- Diferença entre nó **Manager** e nó **Worker** no Swarm

---

## 👤 Autor

**George Abreu**
[![GitHub](https://img.shields.io/badge/GitHub-George--Abreu--git-181717?style=flat&logo=github)](https://github.com/George-Abreu-git)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Conectar-0077B5?style=flat&logo=linkedin)](https://linkedin.com/in/george-abreu-siqueira)
