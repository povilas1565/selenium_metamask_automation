

## selenium_metamask_automation
Этот пакет создан для автоматизации расширения метамаски для криптокошельков с использованием selenium webdriver.

#### Для установки:


```sh
pip install ./selenium_metamask_automation
```
or
```sh
pip install -i https://test.pypi.org/simple/ selenium-metamask-automation
```
Проверить, существует ли пакет
```sh
pip list
```

## Функции

#### 1. Чтобы скачать расширение:

```sh
selenium_metamask_automation.downloadMetamaskExtension()
```

Эта функция должна быть запущена один раз перед всеми функциями для загрузки расширения метамаски. Если вы измените каталог или создадите файл python в другом месте, его необходимо запустить первым, иначе будет выдано следующее исключение:
“Путь к расширению не существует”

#### 2.
Для запуска расширения используйте функцию ниже
```sh
selenium_metamask_automation.launchMetamaskExtension(args)
```
args: путь до chrome webdriver



Эта функция возвращает значение, содержащее драйвер. Вы можете получить его как:
```sh
driver = launchSeleniumWebdriver(r‘C:\Drivers\chromedriver_win32\chromedriver.exe’)
```


Теперь использование может вызывать любой метод selenium, используя эту переменную драйвера.
```sh
driver.get("https://google.com")
```
#### 3. Импорт кошелька
```sh
selenium_metamask_automation.metamaskSetup(arg1, arg2)
```
arg1 : seed phrase of wallet
arg2: password of wallet


#### 4. Чтобы изменить сеть метамаски:
```sh
selenium_metamask_automation.changeMetamaskNetwork(arg)
```

arg: network name

Имена сетей указаны ниже. При выборе любой другой сети выдает ошибку.

- Ethereum Mainnet
- Ropsten Test Network
- Kovan Test Network
- Rinkeby Test Network
- Goerli Test Network

#### 4. Для подключения к любому веб-сайту используйте функцию ниже:
```sh
selenium_metamask_automation.connectToWebsite()
```


Чтобы использовать эту функцию, вы должны сначала посетить веб-сайт
```sh
driver.get("https://google.com")
selenium_metamask_automatiom.connectToWebsite()
```

#### 6. Для подтверждения транзакций:

Подтвердить: 
```sh 
selenium_metamask_automation.confirmApprovalFromMetamask()
```

Отклонить: 
```sh 
selenium_metamask_automation.rejectApprovalFromMetamask()
```


#### 7. Для транзакций, кроме одобрения:

Подтвердить: 
```sh
selenium_metamask_automation.confirmTransactionFromMetamask()
```

Отклонить: 
```sh
selenium_metamask_automation.rejectTransactionFromMetamask()
```

#### 8. Чтобы добавить токен в свой кошелек метамаски:

```sh
selenium_metamask_automation.addToken(arg)
```
arg: contract address of token

#### 9.Знак:

signConfirm: 
```sh
selenium_metamask_automation.signConfirm()
```
signReject: 
```sh
selenium_metamask_automation.signReject()
```


### Ошибки, с которыми вы можете столкнуться:

pip list показывает пакет ```“selenium_metamask_automation”``` но ваша IDE не обнаруживает пакет

##### Решение:

Идти в IDE settings > Python Interpreter 

Изменить путь на C://ProgramFiles//Python//python.exe или добавить в путь, где установлен python.exe
