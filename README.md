# Kind

### Criar cluster no Kind:

- `git clone git@github.com:diegofnunesbr/kind.git`
- `cd kind`
- `kind create cluster --config install.yaml`

### Configurar o NGINX Ingress Controller no Kind:

- `kubectl apply -f ingress-nginx.yaml`

### Remover cluster no Kind:

- `kind delete cluster`
