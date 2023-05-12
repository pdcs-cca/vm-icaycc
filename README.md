# vm-icaycc
Creación de MV para cursos en el instituto

* Creación de MV con VirtualBox y  Debian 11.7
* Se crea el usario `usuario01` que pertenece al grupo sudo en el sistema

## (root) Instalación de paquetes adicionales
~~~bash
apt install vim git build-essential ca-certificates coreutils \
curl environment-modules gfortran git gpg lsb-release python3 \
python3-distutils python3-venv unzip zip flex bison
~~~

## (root) Ajustes al formato del historial
~~~bash
cat /etc/profile.d/icaycc.sh 
export HISTSIZE=500000
export HISTFILESIZE=500000
export HISTCONTROL="erasedups:ignoreboth"
export HISTTIMEFORMAT='%F %T '
export PROMPT_COMMAND="history -a; history -c ; history -r" 
shopt -s histappend
shopt -s cmdhist
~~~

## (usuario01) Instalación y configuración de spack

~~~bash
export SPACK_ROOT=$HOME/spack
echo "export SPACK_ROOT=$SPACK_ROOT" >> $HOME/.bashrc
echo "source $SPACK_ROOT/share/spack/setup-env.sh" >> $HOME/.bashrc
git clone -c feature.manyFiles=true https://github.com/spack/spack.git
source $SPACK_ROOT/share/spack/setup-env.sh
spack compiler find 
spack compilers
~~~


