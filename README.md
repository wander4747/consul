##### inicia o agente
```sh consul agent -dev  ```


##### lista todos nodes
```sh consul members ```

##### acessa a api
```sh curl localhost:8500/v1/catalog/nodes ```


##### criando cluster =cria cluster. ifconfig. crie o diretorio: mkdir /etc/consul.d e /var/lib/consul
```sh consul agent -server -bootstrap-expect=3 -node=consulserver01 -bind=172.21.0.2 -data-dir=/var/lib/consul -config-dir=/etc/consul.d ```

##### join consul
```sh consul join <IP> ``` Ex: consul join 172.21.0.3

##### criando client
```sh consul agent  -bind=172.21.0.5 -data-dir=/var/lib/consul -config-dir=/etc/consul.d ```

```sh consul agent  -bind=172.21.0.6 -data-dir=/var/lib/consul -config-dir=/etc/consul.d -retry-join=172.21.0.5 ``` Ex: pode usar varios retry-join

##### reload
```sh consul reload ```

##### gera chave
```sh consul keygen ```


##### quando tem json
```sh consul agent   -config-dir=/etc/consul.d ```

