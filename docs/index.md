# Contribuindo

For full documentation visit [mkdocs.org](https://mkdocs.org).

## Instalação
Instalar com um gerenciador de pacotes
Se você tem e usa um gerenciador de pacotes (como apt-get , dnf , homebrew , yum , chocolatey , etc.) para instalar pacotes em seu sistema, então você pode querer procurar por um pacote "MkDocs" e, se um recente versão está disponível, instale-a com o seu gerenciador de pacotes (verifique a documentação do seu sistema para obter detalhes). É isso aí, está feito! Pule para Introdução .

Se o seu gerenciador de pacotes não tiver um pacote "MkDocs" recente, você ainda poderá usar o gerenciador de pacotes para instalar o "Python" e o "pip". Então você pode usar o pip para instalar o MkDocs .

Instalação manual
Para instalar manualmente o MkDocs você precisará do Python instalado em seu sistema, assim como o gerenciador de pacotes Python, pip . Você pode verificar se você já instalou esses itens a partir da linha de comando:
```
$ python --version
Python 2.7.2
$ pip --version
pip 1.5.2
```

> O MkDocs suporta as versões 2.7, 3.4, 3.5, 3.6, 3.7 e pypy do Python.

## Instalando o MkDocs
Instale o mkdocspacote usando pip:
```
pip install mkdocs
```

Agora você deve ter o mkdocscomando instalado em seu sistema. Corra mkdocs
--versionpara verificar se tudo funcionou bem.

```
$ mkdocs --version
mkdocs, version 0.15.3
```

## Ambiente de Teste
Há um único arquivo de configuração nomeado mkdocs.ymle uma pasta chamada  docsque conterá seus arquivos de origem da documentação. No momento, a docs pasta contém apenas uma única página de documentação, chamada index.md.

O MkDocs vem com um servidor de desenvolvimento integrado que permite visualizar sua documentação enquanto você trabalha nela. Verifique se você está no mesmo diretório que o mkdocs.yml arquivo de configuração e inicie o servidor executando o mkdocs serve comando:

```
$ mkdocs serve
INFO    -  Building documentation...
INFO    -  Cleaning site directory
[I 160402 15:50:43 server:271] Serving on http://127.0.0.1:8000
[I 160402 15:50:43 handlers:58] Start watching changes
[I 160402 15:50:43 handlers:60] Start detecting changes
```

> Abra http://127.0.0.1:8000/no seu navegador e você verá a página inicial padrão sendo exibida:

## Deploy
Para publicar as modificações realizadas no Github Pages, após adicioná-las ao controle de versão, utilizar o comando **mkdocs gh-deploy**. Ele realizará automaticamente o push das modificações para a branch gh-pages, e em alguns segundos as mudanças estarão disponíveis no site.

```
$ mkdocs gh-deploy
```
