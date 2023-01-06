# CheckUser

*CheckUser* E um verificador de usuários.

# Modo de instalação
```
apt-get update && apt-get install git -y
```
```
python3 -m pip install git+https://github.com/Garagemty
/
gl-CheckUser
```
```
checkuser --config-port 5000 --start --daemon
```

### Ou
```
bash <(curl -sL https://raw.githubusercontent.com/url='https://github.com/Garagemty
/
gl/CheckUser'

CD ~

E se ! [ -x "$(comando -v git)" ]; então
    echo 'Erro: git nao esta instalado.' >&2
    echo 'Instalando Git...'

    sudo apt-get install git -y 1>/dev/null 2>/dev/null

    E se ! [ -x "$(comando -v git)" ]; então
        echo 'Erro: git nao esta instalado.' >&2
        saída 1
    fi

    echo 'Git instalado com sucesso.'
fi

function install_checkuser() {
    echo 'Instalando CheckUser...'

    git clone $ url
    cd CheckUser

    python3 setup.py instalação

    E se ! [ -x "$(comando -v checkuser)" ]; então
        echo 'Erro: CheckUser não está instalado.' >&2
        saída 1
    fi

    Claro
    read -p 'Porta: ' -e -i 5000 porta
    checkuser --port $port --start --daemon

    echo 'CheckUser instalado com sucesso.'
    echo 'Executar: checkuser --help'
    echo 'URL: http://'$(curl -s icanhazip.com)':'$porta
    ler
}

função desinstalar_checkuser() {
    echo 'Desinstalando CheckUser...'

    checkuser --stop

    [[ -d CheckUser ]] && rm -rf CheckUser

    [[ -f /usr/bin/checker ]] && {
        serviço check_user parar
        /usr/bin/checker --uninstall
        rm /usr/bin/verificador
    }

    [[ -f /usr/local/bin/checkuser ]] && {
        serviço check_user parar
        /usr/local/bin/checkuser --remove-service
        rm /usr/local/bin/checkuser
    }
}

função reinstalar_checkuser() {
    desinstalar_checkuser
    install_checkuser
}

função console_menu() {
    Claro
    echo 'CHECKUSER MENU'
    echo '[01] - Instalar CheckUser'
    echo '[02] - Desinstalar CheckUser'
    echo '[03] - Reinstalar CheckUser'
    echo '[00] - Sair'

    read -p 'Escolha uma opção: ' opção

    caso $opção em
    01 | 1)
        install_checkuser
        console_menu
        ;;
    02 | 2)
        desinstalar_checkuser
        console_menu
        ;;
    03 | 3)
        reinstalar_checkuser
        console_menu
        ;;
    00 | 0)
        echo 'Saindo...'
        saída 0
        ;;
    *)
        echo 'Opção inválida.'
        read -p 'Pressione enter para continuar...'
        console_menu
        ;;
    esac

}

função principal() {
    caso $ 1 em
    instalar)
        install_checkuser
        ;;
    atualizar)
        checar atualização
        ;;
    Desinstalar)
        desinstalar_checkuser
        ;;
    *)
        echo 'Uso: ./install.sh [instalar|atualizar|desinstalar]'
        saída 1
        ;;
    esac
}

se [[$# -eq 0]]; então
    console_menu
outro
    principal $ 1
fi/install.sh)
```
 *Opcao 1*

# Atualização
```
python3 -m pip install --upgrade git+https://github.Garagemty
/
gl-CheckUser
```

### Ou
```
bash <(curl -sL https://raw.githubusercontent.com/Garagemty
/
gl/install.sh)
```
 *Opcao 2*

# Como usar
```
checkuser --help
```
