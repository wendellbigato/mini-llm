### Manual de Criação de Ambiente para Mini LLM com 10 Parâmetros

Este manual descreve todos os passos necessários para configurar um ambiente Python 3.11 usando Anaconda, instalar os pacotes necessários e resolver dependências antes de iniciar o desenvolvimento de um mini LLM com 10 parâmetros.

#### 1. Instalar Anaconda

Se você ainda não tem o Anaconda instalado, baixe e instale a partir do site oficial: [Anaconda](https://www.anaconda.com/products/distribution).

#### 2. Criar um Ambiente com Python 3.11 no Anaconda

Abra o Anaconda Prompt e execute os seguintes comandos para criar e ativar um ambiente com Python 3.11:

```sh
conda create --name mini-llm-env python=3.11
conda activate mini-llm-env
```

#### 3. Instalar Jupyter Notebook

Instale o Jupyter Notebook no seu novo ambiente:

```sh
conda install jupyter
```

#### 4. Instalar Bibliotecas Necessárias

Execute os seguintes comandos para instalar as bibliotecas `numpy` e `tensorflow`:

```sh
pip install numpy tensorflow
```

#### 5. Resolver Dependências

Durante a instalação, podem surgir advertências sobre dependências não resolvidas. Para resolver essas dependências, execute os seguintes comandos:

```sh
pip install filelock fsspec pyyaml tqdm contourpy cycler fonttools kiwisolver pillow pyparsing python-dateutil sympy portalocker
```

#### 6. Resolver Conflitos de Dependências com `awscli`

Se houver conflitos de dependências com `awscli`, siga os passos abaixo para resolver:

1. **Desinstalar a versão atual de `botocore`**:

   ```sh
   pip uninstall botocore
   ```

2. **Instalar a versão específica de `botocore`**:

   ```sh
   pip install botocore==1.34.97
   ```

3. **Instalar `colorama`**:

   ```sh
   pip install colorama
   ```

#### 7. Verificar a Instalação dos Pacotes

Após instalar os pacotes adicionais, verifique se todos os pacotes necessários estão instalados corretamente e se não há mais dependências ausentes:

```sh
pip list
```

Aqui está a lista completa de pacotes instalados e suas versões:

```plaintext
Package                      Version
---------------------------- -----------
absl-py                      2.1.0
astunparse                   1.6.3
awscli                       1.32.97
botocore                     1.34.97
certifi                      2024.7.4
charset-normalizer           3.3.2
colorama                     0.4.6
coloredlogs                  15.0.1
contourpy                    1.2.1
cycler                       0.12.1
dnspython                    2.6.1
docutils                     0.16
email_validator              2.2.0
filelock                     3.15.4
flatbuffers                  24.3.25
fonttools                    4.53.1
fsspec                       2024.6.1
gast                         0.6.0
google-pasta                 0.2.0
grpcio                       1.65.4
h5py                         3.11.0
httptools                    0.6.1
huggingface-hub              0.23.4
idna                         3.7
iopath                       0.1.10
jmespath                     1.0.1
kaleido                      0.2.1
keras                        3.4.1
kiwisolver                   1.4.5
libclang                     18.1.1
Markdown                     3.6
markdown-it-py               3.0.0
MarkupSafe                   2.1.5
matplotlib                   3.9.1
mdurl                        0.1.2
ml-dtypes                    0.4.0
mpmath                       1.3.0
namex                        0.0.8
numpy                        1.26.4
nvidia-cudnn-cu12            8.9.2.26
nvidia-cusolver-cu12         11.4.5.107
onnxruntime                  1.18.1
opt-einsum                   3.3.0
optree                       0.12.1
packaging                    24.1
pillow                       10.4.0
pillow_heif                  0.16.0
pip                          24.0
portalocker                  2.10.1
protobuf                     4.25.4
Pygments                     2.18.0
pyparsing                    3.1.2
python-dateutil              2.9.0.post0
python-dotenv                1.0.1
PyYAML                       6.0.1
requests                     2.32.3
rich                         13.7.1
rsa                          4.7.2
s3transfer                   0.10.1
setuptools                   69.5.1
shellingham                  1.5.4
six                          1.16.0
starlette                    0.37.2
sympy                        1.13.1
tensorboard                  2.17.0
tensorboard-data-server      0.7.2
tensorflow                   2.17.0
tensorflow-io-gcs-filesystem 0.37.1
termcolor                    2.4.0
tqdm                         4.66.5
typing_extensions            4.12.2
urllib3                      2.2.2
uvicorn                      0.30.1
uvloop                       0.19.0
watchfiles                   0.22.0
websockets                   12.0
Werkzeug                     3.0.3
wheel                        0.43.0
wrapt                        1.16.0
```

#### 8. Iniciar o Jupyter Notebook

Finalmente, para iniciar o desenvolvimento do seu mini LLM, inicie o Jupyter Notebook:

```sh
jupyter notebook
```

