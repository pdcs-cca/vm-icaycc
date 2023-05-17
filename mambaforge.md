# Mambaforge

Descargar el instalador de mambaforge e instalar en el directorio actual:

~~~bash
curl -LO# https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-Linux-x86_64.sh

bash Mambaforge-Linux-x86_64.sh -b -p $HOME/mambaforge
~~~

La instalación en modo no interactivo, opción `-b`, no modifica el archivo `.bashrc` por lo que para el uso de mamba se debe ejecutar lo siguiente:

~~~bash
source $HOME/mambaforge/etc/profile.d/conda.sh
conda activate base
~~~

Se recomienda cargar el entorno manualmente y no de forma autómatica mediante el archivo .bashrc para evitar posibles conflictos con otros paquetes de software

