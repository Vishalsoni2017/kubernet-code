 <b>Kubernetes command</b>
1. kubectl cluster-info
2. kubectl get all
3. kubectl get node
4. kubeclt get pod --all-namespaces
5. kubectl create -f file_name.yml
6. kubectl apply -f file_name.yml
7. kubectl get pod/po/podes
8. kubectl describe pod/metaname_name
9. kubectl logs -f metaname_name
10. kubectl logs -f metaname_name -c continaer_name
11. kubectl exec metaname_name -c container_name -- command(whoami)
12. kubectl exec metaname_name -itc container_name -- bash
13. kubectl get pod metaname_name --show-labels
14. kubectl get pod metaname_name --show-labels
15. kubectl get pod -l label_name=label_value  e.g (env=qa)
16. kubectl get pod -l 'label_name in (label_value)'        e.g 'env in (dev,qa)'
17. kubectl get pod -l 'label_name notin (label_value)'     e.g 'env notin (dev,qa)'
18. kubectl label pod metaname_name label_name=label_value  e.g type=business  
19. kubectl label pod metaname_name label_name-
20. kubectl label node minikube machine=vsoni
21. kubectl run redis -l tier=db --image=redis:alpine
22. kubectl expose pod redis --port=6379 --name redis-service
23. kubectl create deployment  webapp --image=kodekloud/webapp-color --replicas=3
24. kubectl run custom-nginx --image=nginx --port=8080
25. kubectl create ns dev-ns
26. kubectl create deployment redis-deploy --image=redis --replicas=2 -n dev-ns
27. kubectl get po --selector bu=finance
28. kubectl run httpd --image=httpd:alpine --port=80 --expose
29.  $k get pod --selector env=prod,bu=finance,tier=frontend
30.  kubectl taint nodes node01 spray=mortein:NoSchedule
    <h4>Replication Controller</h4>
31. kubectl replace -f file_name.yml
32. kubectl scale --replicas=6 -f file_name.yml
33. kubectl scale --replicas=10 rc -l label_name=label_value  e.g env=qa
34. kubectl scale --replicas=2 rc/metaname_name
35. kubectl edit metaname_name
36. kubectl delete rc metaname_name
    <h4>Replication Set</h4>
37. kubectl get rs
38. kubectl scale --replicas=10 rs/metaname_name
39. kubectl delete rs metaname_name
    <h4>Deployment</h4>
    kubectl explain deployment
    kubectl explain deployment --recursive
    kubectl explain deployment.metadata.name
40. kubectl describe deployment metaname_name
41. kubectl set image deployment/metaname_name nignx=nignx:1.4
42. kubectl edit deployment/metaname_name
43. kubectl rollout  status deployment/metaname_name
44. kubectl rollout history  deployment/metaname_name
45. kubectl delete deployment metaname_name
46. kubectl rollout undo deploy/metaname_name
47. kubectl rollout undo deploy/metaname_name --to-revision=1
48. kubectl rollout pause deployment/hello
49. kubectl rollout resume deployment/hello
50. <h4>Networking</h4>
51. curl localhost:80  -singlepod
52. curl 10.244.0.61:80  --multipod
53. minikube ssh
54. kubectl get svc
55. minikube service myapp-service --url
56. curl http://192.168.49.2:30004
57. kubectl port-forward --address 0.0.0.0 svc/myapp-service 30004:80
    


