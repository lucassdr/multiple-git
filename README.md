# multiple-git

_shell-script_ para trocar com facilidade as múltiplas contas **git**.

## **Versão** `1.0.0`

#

## **Passo a passo**

### **1.** Gere sua chave SSH. Caso não sabia como fazer isto basta seguir [este tutorial.](https://git-scm.com/book/pt-br/v1/Git-no-Servidor-Gerando-Sua-Chave-P%C3%BAblica-SSH)

### **2.** Crie um arquivo com a extensão **`.sh`** em um local de sua preferência. No exemplo o arquivo chama-se **`trocarConta.sh` e encontra-se na pasta raiz do usuário**.

### **3.** Adicione o script abaixo no seu arquivo, substituindo `user01` pelo seu _username_ e `user01@email01.com` pelo seu _email_. Repita o processo para a segunda conta.

_Caso tenha mais de duas contas basta adicionar nova linha do **swicth/case**._

## Script

```sh
## Switch account Git (Personal/Enterprise)

printf 'Escolha a conta git. USER_1: user01 | USER_2: user02:'
printf '\n'
read ACCOUNT

case $ACCOUNT in
	user01)
		USER_NAME="user01"
		USER_EMAIL="user01@email01.com"
		;;
	user02)
      	USER_NAME="user02"
		USER_EMAIL="user02@email02.com"
      	;;
esac

git config user.name $USER_NAME
git config user.email $USER_EMAIL

echo "ALTERADO PARA: "$USER_NAME "("$USER_EMAIL")"
```

### **4.** Para executar basta digitar o nome do arquivo no terminal. No exemplo o comando a ser executado **`~/trocarContaGit.sh`**.

### **5.** Será exibida o texto de ajuda e insira o `username` da conta desejada.

```sh
Escolha a conta git. PESSOAL: user01 | ENTERPRISE: user02:
```

### **6.** Se tudo der certo a seguinte mensagem será exibida:

```sh
ALTERADO PARA: user02 (user02@email02.com)
```

|           |                                                      |
| --------- | ---------------------------------------------------- |
| site      | [lucassdr.com.br](https://lucassdr.com.br)           |
| linkedin  | [IN_lucassdr](https://www.linkedin.com/in/lucassdr/) |
| email     | [@lucassdr](lucassdr@outlook.com.br)                 |
| instagram | [@lucassdr](https://www.instagram.com/lucassdr/)     |
