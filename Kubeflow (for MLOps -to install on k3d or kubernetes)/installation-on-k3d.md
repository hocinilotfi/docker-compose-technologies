Étapes pour installer Kubeflow sur k3d
1. Créer un cluster k3d (si ce n’est pas déjà fait)
```sh
k3d cluster create kubeflow --api-port 6550 -p 8080:80@loadbalancer
```
Si tu as déjà un cluster k3d, passe cette étape.

2. Installer kfctl (Kubeflow CLI)

```sh
wget https://github.com/kubeflow/kfctl/releases/download/v1.8.0/kfctl_v1.8.0_linux.tar.gz
tar -xvf kfctl_v1.8.0_linux.tar.gz
sudo mv kfctl /usr/local/bin/
```
3. Préparer un dossier de travail
```bash
export KF_NAME=kubeflow
export BASE_DIR=${HOME}/kubeflow
export KF_DIR=${BASE_DIR}/${KF_NAME}
mkdir -p ${KF_DIR}
cd ${KF_DIR}
```
4. Télécharger le fichier de configuration Kubeflow pour Kubernetes (avec Istio)
```bash
wget https://raw.githubusercontent.com/kubeflow/manifests/v1.8.0/kfdef/kfctl_k8s_istio.v1.8.0.yaml
```
5. Déployer Kubeflow
```bash
kfctl apply -V -f kfctl_k8s_istio.v1.8.0.yaml
```
Cette étape va installer plusieurs pods, services, CRD dans ton cluster. Cela peut prendre plusieurs minutes.

6. Vérifier que les pods sont bien déployés
```bash
kubectl get pods -n kubeflow
```
Tu devrais voir plusieurs pods en état Running.

7. Accéder à l’interface Kubeflow
Kubeflow utilise Istio par défaut, qui fait du routing sur le port 80.

Dans ton navigateur, ouvre : http://localhost

Tu devrais voir l’interface Kubeflow.

**Remarques importantes**
Par défaut, la sécurité (authentification) peut être désactivée pour faciliter l’accès local.

Si tu veux utiliser un port différent, ajuste la commande k3d cluster create pour exposer ce port.

Pour arrêter le cluster : 
```bash
k3d cluster delete kubeflow
```

