
#Elk Stack a pipeline de dados mais precisos em web analytics . 🐧


#### Procedimento Instalação ####

- 1 Instalar java jdk

- 2 Adicionar repositorio do ELK

# wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | apt-key add -

## apt-get install apt-transport-https

## echo "deb https://artifacts.elastic.co/packages/5.x/apt stable main" |  tee -a /etc/apt/sources.list.d/elastic-5.x.list

## apt-get update &&  apt-get install elasticsearch logstash kibana

# Adicionar configuração presente no projeto de acordo com sua necessidade 

## Testa elastisearch

# - Verifica status

curl 'localhost:9200'


# - Verifica  indices 

curl 'localhost:9200/_cat/indices?v'



#import dashboards 

wget https://artifacts.elastic.co/downloads/beats/beats-dashboards/beats-dashboards-5.6.9.zip


./scripts/import_dashboards -file ./beats-dashboards-5.6.9.zip  -es http://localhost:9200


