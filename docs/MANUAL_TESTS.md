# Main manual test

## Send all coins with wallet
- [ ] 1. ethToken
- [ ] 2. eth
- [ ] 3. btc

## Swap browser2browser
- [ ] 1. swap - btc2eth (balance - btc: full, eth:full)
- [ ] 2. swap - btc2eth (balance - btc: 0, eth:0)
- [ ] 3. swap - btc2ethToken (balance - btc: full, eth:full)
- [ ] 4. swap - btc2ethToken (balance - btc: 0, eth:0)

## Swap browser2bot
- [ ] 1. swap - btc2eth (balance - btc: full, eth:full)
- [ ] 2. swap - btc2eth (balance - btc: 0, eth:0)
- [ ] 3. swap - eth2btc (balance - btc: full, eth:full)
- [ ] 4. swap - eth2btc (balance - btc: 0, eth:0)
- [ ] 5. swap - btc2ethToken (balance - btc: full, eth:full)
- [ ] 6. swap - btc2ethToken (balance - btc: 0, eth:0)
- [ ] 7. swap - ethToken2btc (balance - btc: full, eth:full)
- [ ] 8. swap - ethToken2btc (balance - btc: 0, eth:0)


---


# Complex manual test

выполнять желательно после каждого билда. Прошел тест? Улучши его, добавь чекбоксы

## базовый тест (до 10 минут)
- [ ] 1. зашел на testnet.swap.online, создал ордер SELL BTC , BUY X (вместо X любой рандомный коин, например ETH)
- [ ] 1.1 увидел сразу собственный ордер в спсике своих ордеров
- [ ] 2.0. с другого браузера этот ордер увиедел перейдя по кнопке share
- [ ] 2.1. напрвления "ю бай" и "ю селл" в обоих браузерах показываются нормально а не перепутано
- [ ] 3. куллер не шумит
- [ ] 4. еслли денег достаточно то доступен "плей"
- [ ] 5. нажали "плей" (с браузера яндекс), пошел свап
- [ ] 5.1. в течении нескольких секунд у маркетмейкера появилось уведомление, что кто то хочет начать свап
- [ ] 6.1. нажали крестик "отменить свап" отмена сработала у обоих корректно
- [ ] 6.2 кто то другой попробовал запустить этот свап и не сммог
- [ ] 7. подождали сколько то секунд, начался свап корректно
- [ ] 8. все шаги свапа выполнились


## тест с мобилой (до 10 минут)
- [ ] 9.1 в андроиде создается оредр на продажу 1 свап за 0.00015 btc
- [ ] 9.2 в браузере на компе он виден сразу
- [ ] 9.3 клиент  вбраузере нажимает плей
- [ ] 9.4 сразу приходит уведолмнеие на андроид
- [ ] 9.5 ждем пока свап закончится
- [ ] 9.6 свап закончисля


## тест частичного закрытия
- [ ] 10. маркетмейеер создает ордер указывает галочку частичного закрытия
- [ ] 10.1. ордер появился у второго человека
- [ ] 10.2. если зайти на страницу с партиалскложуре и ввести сумму меньшую чем созданный ордер то появится сумма сколько человек полуит.
- [ ] 10.3. сумма корректная (посчитано в калькуляторе в ручную совпадает с тем что показывает)
- [ ] 10.4 при нажатии на старт приходит уведомление маркетмейкеру, он нажимает на отмену и свап не начинается. пользователь добавляет  этот оредр в игнор и котировка пересчитывается опираясь на другой ордер
- [ ] 10.5 при нажатии на галочку (маркетмейкре согласился) начинается и завершается обычный свап
- [ ] 10.6 проверить, что в истории все пришло верно как на калькуляторе


## тест маркетмейкера (до 5ти минут)
- [ ] 10.1 в браузере создается ордер на продажу 1 свап за 0.00015 BTC
- [ ] 10.2 в браузере создается ордер на покупку 1 свап за 0.0001 BTC (дешевле чем на продажу)
- [ ] с browserstack заходит человек и выполняет оредр 10.1
- [ ] одновременно из андроида пытаемся выполнить ордер 10.2
- [ ] маркетмейкер ничего не делает по идее должен выполнится ордер 10.1, а 10.2 отказатся


## тест альтернатив дестинейшин адрес

//todo


## прочие тесты (нужно расписать подробнее)

- [ ] тест с альтернатив дестинейшин адрес
- [ ] тест с отсутсвием биткоина на счету
- [ ] тест с нулевыми балансами
- [ ] элемент "копировать адрес" работает
- [ ] элемент "обновить баланс" работает
- [ ] если двое одновременно пытаются стартануть со мной свап, то один из них отменится?
- [ ] Проверка кнопок социальных сетей
- [ ] Проверка кнопки уведомлений
- [ ] Проверка суммы переводов в историях
- [ ] Проверка возврата средств при истечении 180 минут при отмены подписания контракта
- [ ] Проверка актуальности ссылок в подвале сайта
- [ ] Проверка стандартной операции отправки валюты


---


# New blockchain Manual Test

тесткейс который позволяет протестировать полностью работает ли обмен на новом блокчейне


## подготовка к тестированию
- [ ] максимально очистите данные браузера: кэш, куки, local storage.
- [ ] после сброса данных браузеров откройте в новой вкладке тестируемый адрес.


## проверка создания адреса
- [ ] при первом посещении главной станицы появляется модальное окно с приватными ключами и с предложением сохранить их двумя способами: сохранить файл с ключами или сделать скриншот окна.
- [ ] при нажатии на кнопку скачивания ключей браузер начинает автоматическую загрузку файла.
- [ ] при нажатии на кнопку "I saved the keys in a safe place" появляется дополнительное модальное окно для финального подтверждения сохранения ключей.
- [ ] при нажатии на нкопку "No" возвращается предыдущее модальное окно приатными ключами и предложением их сохранить.
- [ ] при нажатии на кнопку "Yes" появляется модальное окно с информацией об отказе от ответстенности в случе утери ключей и с кнопками для их сохранения.
- [ ] при нажатии на кнопку "Next step" открывается форма для проверки сохранненых вами ключей.
- [ ] при вводе ключей и их удачной проверке появляется кнопка "go to the site"
- [ ] при нажатии на кнопку "go to the site" открывается стартовая страница Wallet со списком адресов криптовалюты с 0 балансом.


## проверка ввода и вывода средств
- [ ] я отправил деньги извне и они пришли на баланс
- [ ] при нажатии на send показывается форма для ввода адреса и суммы, при этом показано сколько доступно для перевода
- [ ] если ввести сумму меньшую чем минимально возможная отправка то покажется ошибка
- [ ] если ввести сумму большую чем баланс то покажется ошибка
- [ ] форма не принимает левые данные кроме числа
- [ ] при нажатии на кнопку отправки появляется прелоадер
- [ ] как только транзакция замайнится прелоадер исчезает 
- [ ] транзакция на отправку видна в истории


## создание ордера на продажу едениц криптовалюты за биткоин
- [ ] на странице кошелька есть кнопка SWAP, которая означает что можно поменять эту крипту на другую
- [ ] заходим на в свап и виден ордербук (таблица с обьявлениями на покупку и продажу)
- [ ] видна кнопка create order при нажатии на нее появляется форма для создания ордера
- [ ] в форме виден мой доступный баланс и он корректный
- [ ] я хочу продать 10 едениц за 0.1 биткоин, ввожу данные в sell 10 , в buy 0.1 btc автоматически устанавливается курс 100 едениц / BTC 
- [ ] я хочу продать больше чем у меня есть, появляется ошибка
- [ ] если поменять курс то поменяется поле buy, а поле сколько продать (sell) остается неизменным
- [ ] при нажатии далее все данные указаны верно 
- [ ] mining fee тоже указан верно
- [ ] если зайти из другого браузера и попробовать найти этот оредр то он будет виден в корректном месте


## создание ордера на покупку едениц криптовалюты за биткоин
- [ ] хочу купить 100 едениц криптовалюты за 0.1 BTC ввел 100 едениц в поле buy и 0.1 BTC в поле sell все верно выставилось, курс верный (показывает 1000 едениц за BTC)
- [ ] ордер создается


## пробуем свпнутся
- [ ] получилось свопнутся из двух браузеров (обоим в итоге написало "сенкью")
