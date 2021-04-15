
## Exercises

k create namespace ckad
k config set-context --current --namespace=ckad
k run nginx --image=nginx:1.17.0 --port=80 -n ckad
k describe pod nginx -n ckad | grep IP:
k run -it --rm -n ckad wget --image=busybox wget nginx:80
k logs nginx -n ckad