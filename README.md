# ansible-wordpress
Ansible, organização de playbook com wordpress

## Playbooks reaproveitáveis com Roles | Organização de playbook

Com Roles é possível dividir o código em arquivos de forma que possam ser reaproveitados em outros projetos, elas representam uma forma de encapsular tarefas, variáveis e *handlers*
 para facilitar o reuso. para isso é necessário que os arquivos estejam nas pastas buscadas pelo ansible

exemplo de instalação do mysql (em cada pasta deverá conter um arquivo com o nome do host ex: mysql.yml)

pastabase

- roles
    - mysql
        - tasks
            
            tarefas a serem executadas
            
        - handlers
            
            inicialização, reinicialização etc…
            
        - files
            
            ex: arquivos que podem ser copiados para dentro da vm com o módulo copy
            
        - group_vars
            
            ex: varáveis que serão preenchidas
            
        - defaults
            
            valores padrão de variáveis etc…
            
        - meta
            
            lista de dependências da role
