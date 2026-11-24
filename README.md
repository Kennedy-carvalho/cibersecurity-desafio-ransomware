# Desafio Ransomware - Cybersecurity

Projeto prático desenvolvido por **Kennedy Anderson** durante o curso **Cybersecurity Specialist** da DIO, sob orientação do professor **Cassiano Peres**.

O objetivo deste desafio é demonstrar, em um ambiente controlado e seguro, como funciona o processo básico de criptografia e descriptografia de um arquivo utilizando Python e a biblioteca `pyaes`.

## Conteúdo

- [Sobre o projeto](#sobre-o-projeto)
- [Aviso de segurança](#aviso-de-segurança)
- [Tecnologias utilizadas](#tecnologias-utilizadas)
- [Estrutura do projeto](#estrutura-do-projeto)
- [Como executar](#como-executar)
- [Passo a passo](#passo-a-passo)
- [Fluxo do projeto](#fluxo-do-projeto)
- [Evidências](#evidências)
- [Aprendizados](#aprendizados)
- [Referências](#referências)

## Sobre o projeto

O projeto simula o comportamento básico de um ransomware educacional:

1. Lê o conteúdo de um arquivo chamado `teste.txt`.
2. Criptografa os dados com AES no modo CTR.
3. Remove o arquivo original.
4. Cria o arquivo criptografado `teste.txt.ransomwaretroll`.
5. Permite restaurar o arquivo original por meio do script descriptografador.

> Este projeto foi criado exclusivamente para fins educacionais e não deve ser utilizado para criptografar arquivos sem autorização.

## Aviso de segurança

Não execute este projeto em diretórios que contenham informações pessoais ou documentos importantes.

- Utilize apenas uma pasta isolada criada para o desafio.
- Faça uma cópia de segurança do arquivo de teste.
- A chave está incluída diretamente no código, pois este é um projeto didático.
- Não utilize esta implementação como solução real de proteção de dados.

## Tecnologias utilizadas

- Python
- Biblioteca `pyaes`
- Kali Linux
- Terminal Bash
- Nano

## Estrutura do projeto

```text
cibersecurity-desafio-ransomware/
|-- encrypter.py
|-- decrypter.py
|-- teste.txt
|-- evidencias/
|   |-- 1-instalar 2-criar pasta 3-entrar nela 4 criar encrypter decrypter e texto.png
|   |-- 1- encryptando.png
|   |-- Design sem nome.png
|   |-- Design sem nome (1).png
|   |-- Design sem nome (8).png
|   `-- mensgem a ser usada no teste !!.png
`-- README.md
```

## Como executar

### 1. Instalar o Python

No Kali Linux, atualize os pacotes e instale os recursos necessários:

```bash
sudo apt update
sudo apt install -y python3-pyaes
```

Também é possível utilizar `pip`, dependendo do ambiente:

```bash
pip install pyaes
```

### 2. Criar a pasta do projeto

```bash
mkdir projeto-ransomware
cd projeto-ransomware
```

### 3. Criar os arquivos

```bash
touch teste.txt
touch encrypter.py
touch decrypter.py
```

### 4. Adicionar o conteúdo de teste

Abra o arquivo `teste.txt`:

```bash
nano teste.txt
```

Exemplo de conteúdo:

```text
mensagem a ser usada no teste !!

Kennedy Anderson
```

Salve com `Ctrl + O`, confirme com `Enter` e saia com `Ctrl + X`.

## Passo a passo

### Criptografar o arquivo

Execute o script de criptografia:

```bash
python3 encrypter.py
```

O script irá:

1. Ler `teste.txt`.
2. Remover o arquivo original.
3. Criptografar seu conteúdo.
4. Criar `teste.txt.ransomwaretroll`.

### Descriptografar o arquivo

Com o arquivo criptografado presente na mesma pasta, execute:

```bash
python3 decrypter.py
```

O script irá ler `teste.txt.ransomwaretroll`, descriptografar os dados e recriar `teste.txt`.

## Fluxo do projeto

```text
teste.txt
    |
    |  encrypter.py
    v
arquivo criptografado
teste.txt.ransomwaretroll
    |
    |  decrypter.py
    v
teste.txt restaurado
```

## Evidências

### Preparação do ambiente

![Criação da pasta e dos arquivos](<evidencias/1-instalar 2-criar pasta 3-entrar nela 4 criar encrypter decrypter e texto.png>)

### Arquivo de teste

![Conteúdo utilizado no teste](<evidencias/mensgem a ser usada no teste !!.png>)

### Script de criptografia

![Código do encrypter](<evidencias/Design sem nome.png>)

### Processo de criptografia

![Execução da criptografia](<evidencias/1- encryptando.png>)

### Processo de descriptografia

![Restauração do arquivo](<evidencias/Design sem nome (1).png>)

### Resultado final

![Desafio concluído com sucesso](<evidencias/Design sem nome (8).png>)

## Aprendizados

- Manipulação de arquivos em Python com `open`, `read`, `write` e `close`.
- Uso da biblioteca `pyaes` para criptografia AES.
- Funcionamento básico do modo CTR.
- Importância da chave e do estado utilizados durante criptografia e descriptografia.
- Criação de arquivos, execução de scripts e organização de projetos no terminal Linux.
- Identificação dos riscos associados à execução automática e à perda de arquivos.

## Referências

- [Documentação do Python](https://docs.python.org/3/)
- [Repositório do projeto pyaes](https://github.com/ricmoo/pyaes)
- [DIO - Digital Innovation One](https://www.dio.me/)

---

Desenvolvido por **Kennedy Anderson** - Curso **Cybersecurity Specialist**
