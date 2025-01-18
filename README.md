# Repozytorium pracy inżynierskiej

## Opis
Wszystko na razie wrzucone jak leci, także struktura i procedura uruchamiania na razie robocza. Będzie wszystko lepiej zorganizowane (i opisane).

## Wymagania
1. kubernetes itp.
2. kubectl
3. Helm

## Uruchamianie
W domyślnej lokacji w strukturze repozytorium:
```
kubectl apply -f ./mongodb-manual-deploy.yaml
helm install open5gs ./open5gs/ --values ./5gSA-values-test2.yaml
helm install ueransim-gnb oci://registry-1.docker.io/gradiant/ueransim-gnb --version 0.2.6 --values ./gnb-ues-values.yaml
```

## Po zakończeniu
```
helm uninstall ueransim-gnb
helm uninstall open5gs
kubectl rollout restart deployment open5gs-mongodb
```

TODO:
- zrobić po angielsku wersję
- bardziej szczegółowo opisać
- ogarnąć strukturę plików: permanentne zmiany wrzucić do katalogów, a nie values
- pewnie coś na razie przegapiłem i nie działa
