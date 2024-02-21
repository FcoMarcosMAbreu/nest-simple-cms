Para criar a nova branch a partir da branch que você está:
```
git branch MinhaNovaBrach
```

Para criar a nova branch a partir de uma branch especifica:
````
git branch -c branchEspecifica MinhaNovaBrach
````

Nos dois casos você precisa trocar para a branch criada, commitar e fazer o trancking:
````
git checkout MinhaNovaBrach
git commit -m "Olha que commit lindo <3"
git push -u origin MinhaNovaBrach
````
