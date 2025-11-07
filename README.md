# 🚀 Script de Provisionamento de Servidor Web (Apache)

Este projeto é um script Bash para automatizar a configuração completa de um servidor web **Apache2**.

O script cuida de todas as etapas: desde a atualização do sistema e instalação de dependências até a implantação (deploy) de uma aplicação web estática. Este é um exemplo prático de **Infraestrutura como Código (IaC)**.

---

## ⚙️ Funcionalidades

O script foi projetado para executar as seguintes tarefas em sequência:

1.  **Atualizar o Servidor:** Garante que todos os pacotes do sistema (Ubuntu) estejam atualizados.
2.  **Instalar Dependências:** Instala o servidor web `apache2` e o utilitário `unzip`.
3.  **Baixar a Aplicação:** Faz o download de uma aplicação web de exemplo (do repositório de Denilson Bonatti no GitHub) e a salva no diretório `/tmp`.
4.  **Implantação (Deploy):** Descompacta e copia os arquivos da aplicação para o diretório raiz padrão do Apache (`/var/www/html`), tornando o site publicamente acessível.

---

## 🛠️ Como Usar

O script foi projetado para ser executado em um servidor Linux (baseado em Ubuntu) com privilégios de administrador.

### Pré-requisitos
* Um servidor Linux (Ubuntu Server).
* Acesso ao usuário `root` ou um usuário com permissões `sudo`.

### Execução

1.  Clone este repositório (ou apenas crie o arquivo do script no seu servidor):
    ```bash
    # Exemplo de como criar o arquivo
    nano provision-apache.sh
    ```
    (Cole o conteúdo do seu script aqui)

2.  Dê permissão de execução ao script:
    ```bash
    chmod +x provision-apache.sh
    ```

3.  Execute o script com privilégios de administrador:
    ```bash
    sudo ./provision-apache.sh
    ```

### Verificação

Após a execução, o servidor web estará configurado. Você pode verificar o resultado acessando o endereço de IP público do seu servidor em um navegador:

`http://SEU_IP_PUBLICO`

Você deverá ver o site que foi implantado.

---

## 💻 Tecnologias Utilizadas

* **Bash Script (Shell Script)**
* **Apache2** (Servidor Web)
* **Linux (Ubuntu)**
