## Command to gather facts

ansible 172.31.14.132 -m setup

## Command to gater facts by applying filters

``` ansible 172.31.14.132 -m setup -a 'filter=*os*family' ```

## Ansible tags

``` ansible-playbook tags.yml --tags deploy ```

``` ansible-playbook tags.yml --tags deploy,start ```

## Ansible skip tags
``` ansible-playbook tags.yml --skip-tags deploy,start ```

## Retry a playbook only on failed nodes

``` ansible-playbook tags.yml --limit @tags.retry ```

## Ansible forks

``` ansible-playbook tags.yml --forks 10 ```

## Passing variables at command line

``` ansible-playbook apache-vars.yml -e apache_port=2121 ```
