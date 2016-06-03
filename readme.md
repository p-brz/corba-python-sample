# Echo server com CORBA em python

Um exemplo utilizando CORBA em python.

Utiliza a implementação de CORBA [omniORB](https://sourceforge.net/projects/omniorb/).

    omniORB is a robust high performance CORBA ORB for C++ and Python. It is freely available under the terms of the GNU Lesser General Public License (for the libraries), and GNU General Public License (for the tools). omniORB is largely CORBA 2.6 compliant.

Este exemplo foi retirado da [documentação do omniORB para Python](http://omniorb.sourceforge.net/omnipy42/omniORBpy/omniORBpy002.html#toc3)

## Requisitos

É preciso ter os pacotes do omniORB, incluindo bindings para python, para executar o projeto.

No Ubuntu/Linux Mint é possível instalar os seguintes pacotes via Apt:

* python-omniorb
* omniidl
* omniidl-python
* omniorb
* omniorb-nameserver

        sudo apt-get install python-omniorb omniidl omniidl-python omniorb omniorb-nameserver

## Execução

Antes de tudo é preciso "compilar" o arquivo '.idl' para gerar os stubs e skeletons.

        omniidl -bpython echo.idl

Em seguida, para assegurar que o servidor de nomes do omniORB
está executando, utilize o comando:

        omniNames

Por fim, é possível executar o cliente e servidor:

        python echo_impl.py

e

        python echo_client.py
