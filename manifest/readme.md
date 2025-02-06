docker login habor.analytichpxv3.online



docker build . -t habor.analytichpxv3.online/ui:test


docker push habor.analytichpxv3.online/ui:test

kubectl create secret docker-registry regcred --docker-server=docker login https://habor.analytichpxv3.online/ --docker-username=kevvdev --docker-password=Aa112233 --docker-email=kev@hpktechnology.com


kubectl create secret docker-registry --namespace test1 regcred \
  --docker-server=https://habor.analytichpxv3.online/ \
  --docker-username=tensedev \
  --docker-password=Aa112233 \
  --dry-run=client -oyaml > regcred.yaml




kubectl describe pod api-app-5f9c5d4f9f-chhsv  -n dev


kubectl port-forward -n dev svc/api-app-service 8080:8080