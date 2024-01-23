 <b>Kubernetes command</b>
1. kubectl cluster-info
2. kubectl get all
3. kubectl get node
4. kubectl create -f file_name.yml
5. kubectl apply -f file_name.yml
6. kubectl get pod/po/podes
7. kubectl describe pod/metaname_name
8. kubectl logs -f metaname_name
9. kubectl logs -f metaname_name -c continaer_name
10. kubectl exec metaname_name -c container_name -- command(whoami)
11. kubectl exec metaname_name -itc container_name -- bash
12. kubectl get pod metaname_name --show-labels
13. kubectl get pod metaname_name --show-labels
14. kubectl get pod -l label_name=label_value  e.g (env=qa)
15. kubectl get pod -l 'label_name in (label_value)'        e.g 'env in (dev,qa)'
16. kubectl get pod -l 'label_name notin (label_value)'     e.g 'env notin (dev,qa)'
17. kubectl label pod metaname_name label_name=label_value  e.g type=business  
18. kubectl label pod metaname_name label_name-
19. kubectl label node minikube machine=vsoni
    <h4>Replication Controller</h4>
21. kubectl replace -f file_name.yml
22. kubectl scale --replicas=6 -f file_name.yml
23. kubectl scale --replicas=10 rc -l label_name=label_value  e.g env=qa
24. kubectl scale --replicas=2 rc/metaname_name
25. kubectl edit metaname_name
26. kubectl delete rc metaname_name
    <h4>Replication Set</h4>
28. kubectl get rs
29. kubectl scale --replicas=10 rs/metaname_name
30. kubectl delete rs metaname_name
    <h4>Deployment</h4>
    kubectl explain deployment
    kubectl explain deployment --recursive
    kubectl explain deployment.metadata.name
32. kubectl describe deployment metaname_name
33. kubectl set image deployment/metaname_name nignx=nignx:1.4
34. kubectl edit deployment/metaname_name
35. kubectl rollout  status deployment/metaname_name
36. kubectl rollout history  deployment/metaname_name
37. kubectl delete deployment metaname_name
38. kubectl rollout undo deploy/metaname_name
39. kubectl rollout undo deploy/metaname_name --to-revision=1
40. kubectl rollout pause deployment/hello
41. kubectl rollout resume deployment/hello
42. <h4>Networking</h4>
43. curl localhost:80  -singlepod
44. curl 10.244.0.61:80  --multipod
45. minikube ssh
46. kubectl get svc
47. minikube service myapp-service --url
48. curl http://192.168.49.2:30004
49. kubectl port-forward --address 0.0.0.0 svc/myapp-service 30004:80
    


