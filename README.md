# Kind

Este guia descreve a instalação e remoção do **Kind** em sistemas Linux, incluindo a criação de um cluster Kubernetes pronto para uso com o **kubectl**.

## Instalar dependências

### Docker

```bash
curl -fsSL https://get.docker.com | sh
sudo usermod -aG docker $USER
```

### kubectl

```bash
curl -LO "https://dl.k8s.io/release/$(curl -Ls https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
```

## Instalar o Kind

```bash
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.23.0/kind-linux-amd64
chmod +x kind
sudo mv kind /usr/local/bin/kind
```

## Criar o cluster Kind

```bash
git clone https://github.com/diegofnunesbr/kind.git
kind create cluster --name k8s --config kind/kind.yaml
```

## Remover o cluster Kind

```bash
kind delete cluster --name k8s
```

## Remover o Kind

```bash
sudo rm -rf /usr/local/bin/kind
```
