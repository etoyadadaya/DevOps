## Container orchestration:

1. В чем преимущества Kubernetes как платформы?

2. Что такое control plane и из каких компонентов состоит?

3. Какие CNI вы использовали, и чем они отличаются?

4. Чем отличается managed Kubernetes от self-deployed?

5. Как можно контролировать размещение подов в кластере? (taints/tolerations, affinities, topologies etc.)

6. Скейлинг кластера. Cluster autoscaler vs HPA vs VPA? Как сделать zero-downtime node decommission/cluster upgrade? PDB? Lifecycle hooks?

7. Какие способы для внешнего доступа к кластеру? ingress, node port, port-forward и т. д.

8. С каким PID запускается процесс в контейнере?

9. Что лучше использовать для изоляции окружения – Vagrant или Docker?

10. Какой инструмент оркестрирования контейнеров использовали? (Swarm, Kubernetes, Openshift, Rancher и т. д.)

11. Что происходит в Kubernetes после запуска kubectl (API, ReplicaSet Controller, storage back-end, scheduler, kubelet, worker node, pod)?

12. Какая разница между pod и контейнером в K8s?

13. Как мы можем сделать любой микросервис, работающий на K8s, доступным из внешней среды?
