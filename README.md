# Ansible Role: Elasticsearch

Ansible role for installing Elasticsearch on CentOS

## Requirements
Oracle JVM 1.8u40+

or

IcedTea OpenJDK 1.8.0.91+

## Variables
|Variable Name | Default Value |
|:------------|:-------|
`es_yum_repo_baseurl` | `https://artifacts.elastic.co/packages/5.x/yum`
`es_yum_repo_gpgkey` | `https://artifacts.elastic.co/GPG-KEY-elasticsearch`
`es_cluster_name` | `elasticsearch`
`es_node_name` | [`inventory_hostname`](http://docs.ansible.com/ansible/latest/playbooks_variables.html#magic-variables-and-how-to-access-information-about-other-hosts)
`es_data_path` | `/var/lib/elasticsearch`
`es_log_path` | `/var/log/elasticsearch`
`es_network_host` | `localhost`
`es_http_port` | `9200`

## Usage
```
roles:
  - role: erumble.elasticsearch
    es_network_host: 0.0.0.0
```
