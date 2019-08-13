# multiple-git

_shell-script_ para trocar com facilidade as múltiplas contas **git**.

## **Versão** `1.0.0`

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

|           |                                       |
| --------- | ------------------------------------- |
| site      | www.lucassdr.com.br                   |
| linkedin  | https://www.linkedin.com/in/lucassdr/ |
| email     | lucassdr@outlook.com.br               |
| instagram | @lucassdr                             |
