# ansible-operations

Este repositorio es para aquellos playbooks útiles en el soporte y la operación de componentes

Configuración global
ansible.cfg
remote_user = mb67067
forks = 20
host_key_checking = False

Copiar las llaves a los equipos implicados
ansible-playbook Deploy_LLaves_SSH.yml -e "equipos=mx_liga_oculta" -k

Ejecuta validación
ansible-playbook ASO_validaciones_hash_master.yml --extra-vars "lib=resultado_librerias_hash.yml maquinas=mx_laboratorio,mx_test,mx_calidad,mx_octa,mx_liga_oculta" --skip-tags debugging

