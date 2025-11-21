| Характеристика        | Minikube                                                                           | Kind                                                        | K3d                                                                      |
|-----------------------|------------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------|
| Базовий механізм      | VM (за замовчуванням), Docker, bare metal                                          | Docker контейнери (контейнер як нода)                       | Docker контейнери (контейнер як нода, на базі k3s)                       |
| Підтримувані ОС       | Windows, macOS, Linux                                                              | Windows, macOS, Linux                                       | Windows, macOS, Linux                                                    |
| Архітектури           | x86-64, ARM64, ARM                                                                 | x86-64, ARM64                                               | x86-64, ARM64                                                            |
| Багатонодовість       | Обмежена (можна налаштувати, але не є основним сценарієм)                          | Так (основна перевага)                                      | Так (основна перевага)                                                   |
| Автоматизація (CI/CD) | Складно інтегрувати через залежність від VM                                        | Добре (нативний Docker)                                     | Дуже добре (швидкий, нативний Docker/k3s)                                |
| Додаткові функції     | Вбудовані аддони (dashboard, ingress, registry), легке перемикання між драйверами. | Фокусується на мінімалізмі та відповідності ванільному K8s. | Вбудований Registry, проста робота з Ingress, менше споживання ресурсів. |
| Ядро Kubernetes       | Ванільний K8s                                                                      | Ванільний K8s                                               | K3s (легковаговий)                                                       |


# Conclusion
Conclusion is to use k3d 
Pros: 
Cons:
Висновок треба юзати k3d

```

choco install k3d

# Створення кластера
k3d cluster create asciiartify-cluster

# Перевірка
kubectl get nodes

# Деплой Hello World
kubectl create deployment hello-world --image=nginx
kubectl expose deployment hello-world --port=80 --type=NodePort

# Отримати URL
kubectl get svc

```

# Demo
demo with Hello World

<img width="1184" height="752" alt="image" src="https://github.com/user-attachments/assets/93218ebb-e1e6-4d97-8cb1-bb6d85d03157" />



