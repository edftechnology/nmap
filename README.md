# Como configurar/instalar o `nmap` e o `zenmap` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar o `nmap` e o `zenmap` no `Linux Ubuntu`.

## _Abstract_

_In this document are contained the main commands and settings to set up/install the `nmap` and the `zenmap` on `Linux Ubuntu`._

## Descrição [2]

### `nmap`

O `Nmap`, também conhecido como Network Mapper, é uma popular ferramenta de código aberto usada para mapear e avaliar redes de computadores. Ele é amplamente utilizado por administradores de rede, profissionais de segurança cibernética e pesquisadores para descobrir dispositivos ativos em uma rede, identificar portas abertas e serviços em execução nesses dispositivos, além de realizar varreduras de vulnerabilidades e auditorias de segurança. O `Nmap` oferece uma variedade de recursos avançados, incluindo detecção de sistemas operacionais, detecção de versões de serviços e capacidade de scripting para personalizar e automatizar tarefas de varredura. É uma ferramenta essencial para a descoberta e avaliação de redes e sistemas em ambientes de TI e segurança cibernética.

### `zenmap`

O `Zenmap` é uma interface gráfica de código aberto para o scanner de rede `Nmap`, uma das ferramentas de segurança e exploração de rede mais conhecidas e poderosas. O Zenmap simplifica o uso do `Nmap`, permitindo que os usuários realizem varreduras de rede e avaliem a segurança de sistemas e dispositivos de maneira mais intuitiva e visual. Ele fornece recursos avançados, como varreduras de portas, detecção de serviços, identificação de sistemas operacionais e mapeamento de redes, exibindo os resultados em um formato fácil de entender. O Zenmap é usado por profissionais de segurança, administradores de rede e entusiastas da tecnologia para avaliar a postura de segurança de redes e identificar possíveis vulnerabilidades. Suas funcionalidades são altamente configuráveis e podem ser usadas tanto para fins de auditoria de segurança quanto para administração de redes.

## 1. Como configurar/instalar o `nmap` e o `zenmap` no `Linux Ubuntu` [1]

Para configurar/instalar o `nmap` e o `zenmap` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.2 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.3 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update -y`

    2.4 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.5 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update -y`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`

    2.6 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.7 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

### 1.1 `nmap`

Para instalar o `nmap` no `Linux Ubuntu`, você pode seguir estas etapas usando o terminal:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```


2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando:
    ```bash
    sudo apt clean
    ```
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do `cache` local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando:
    ```bash
    sudo apt autoclean
    ```

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando:
    ```bash
    sudo apt autoremove -y
    ```

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt update
    ```

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes:
    ```bash
    sudo apt --fix-broken install
    ```

    2.6 Limpar o `cache` do gerenciador de pacotes `apt` novamente:
    ```bash
    sudo apt clean
    ```
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt list --upgradable
    ```

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt full-upgrade -y
    ```
  

3. Após a atualização, você pode instalar o `nmap` usando o seguinte comando: `sudo apt install nmap -y`

4. O sistema solicitará sua senha de administrador (`sudo`) para confirmar a instalação. Digite sua senha e pressione `"Enter"`.

5. Aguarde até que o processo de instalação seja concluído. O `nmap` será baixado e instalado em seu sistema.

6. Para verificar se o `nmap` foi instalado com sucesso, você pode executar o seguinte comando: `nmap --version`

    Isso exibirá a versão do `nmap` instalada em seu sistema.

Agora, você deve ter o `nmap` instalado em seu sistema `Linux Ubuntu` e pode começar a usá-lo para verificar portas e fazer análises de rede.

#### 1.1.1 Código completo para configurar/instalar

Para instalar o `nmap` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt autoclean
    sudo apt autoremove
    sudo apt update -y
    sudo apt autoremove
    sudo apt autoclean
    sudo apt list --upgradavle
    sudo apt full-upgrade -y
    sudo apt install nmap -y
    sudo apt update -ynmap --version
    ```


## 1.2 `zenmap`

O `zenmap` **NÃO** vem pré-instalado no `Kali Linux` nem no `Linux Ubuntu`. Sendo assim, para instalar o `nmap` tant no `Kali Linux` quanto no `Linux`, siga as instruções no site: https://nmap.org/

Para instalar um arquivo RPM como o zenmap-7.94-1.noarch.rpm em um sistema Linux Ubuntu, você precisará converter o pacote RPM em um formato adequado para o Ubuntu, que é o formato DEB. Você pode fazer isso usando a ferramenta alien. Aqui estão os passos para fazer a conversão e instalação:

1. Instale a ferramenta alien se ainda não estiver instalada. Abra o terminal e execute o seguinte comando para instalar o alien:

    ```
    sudo apt update`
    sudo apt install alien
    ```

2. Após a instalação do `alien`, você pode usar o seguinte comando para converter o arquivo RPM em um pacote DEB: `sudo alien -d zenmap-7.94-1.noarch.rpm`

    Isso criará um arquivo DEB chamado `zenmap_7.94-2_all.deb` (o número da versão pode variar dependendo da versão do `Zenmap`) no diretório atual.

3. Agora você pode instalar o pacote DEB usando o seguinte comando: `sudo dpkg -i zenmap_7.94-2_all.deb`

    Substitua `"zenmap_7.94-2_all.deb"` pelo nome exato do arquivo DEB gerado no passo anterior.

4. Após a instalação ser concluída, você pode iniciar o `Zenmap` a partir do terminal digitando: `zenmap`

O `Zenmap` também pode ser encontrado em seu menu de aplicativos, dependendo do ambiente de desktop que você está usando.

Isso deve permitir que você instale o `Zenmap` a partir do arquivo RPM no Ubuntu usando o `alien` para a conversão do pacote. Certifique-se de que todas as dependências sejam atendidas após a instalação.

## Referências

[1] OPENAI. ***Instalar o Nmap no Linux.*** Disponível em: <https://chat.openai.com/c/375a616c-70f1-498d-b344-968c22e4a4de> (texto adaptado). Acessado em: 02/02/2024 12:16.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 02/02/2024 12:16.

