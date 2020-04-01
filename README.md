
## УСТАНОВКА МОДУЛЯ

- Заходим по ссылке (http://Ваш.домен/plugins)

- Если данного модуля нет в списке -> Обновляем список модулей
	![](/img/update_mods.png "update module")
	
- Устанавливаем модуль который появился после обновления 
	![](/img/install_mod.png "install module")
	
- Активируем модуль
	![](/img/activate_mod.png "active module")


## НАСТРОЙКА МОДУЛЯ

- В настройках модуля копируем URL для Вэбхуков
	![](/img/url_webhook.png "url webhook")
	
- Переходим по ссылке в личный кабинет nextel https://my.nextel.com.ua/index.html#api

- Добавляем по 1му событию: Новый звонок, Звонок перенаправлен, Ответ на звонок, Звонок завершен
	![](/img/add_event.png "add event")
	
- Вставляем в каждое поле события ссылку которую скопировали в CRM "URL для Вэбхуков" - 
- На этой же странице создаем ключ api nextel
	 ![](/img/create_key.png "create key")
* копируем его и вставляем в настройки модуля nextel в CRM


---


## ПОДКЛЮЧЕНИЕ ВХОДЯЩИХ И ИСХОДЯЩИХ ЗВОНКОВ В ЦРМ

- Для принятия и осуществления звонков пользователю в CRM нужно присвоить номер sip - 
	![](/img/operator_settings.png "operator_settings")
он должен соответствовать номеру установленным в софтфоне

- По этой ссылке можно получить данные пользователя sip телефона https://my.nextel.com.ua/index.html#users
( Настройка sip детально описана на сайте nextel https://nextel.com.ua/blog/knowledgebase )


#### Исходящие звонки

- для осуществления звонка переходим в карточку заказа
	![](/img/call_nextel.png "call_nextel")
выбираем nextel, далее если все настроено правильно в црм отобразиться всплывающее окошко и на Ваш софтфон будет осуществлен звонок - 
	![](/img/test_call.png "test_call")
после принятия вызова - начнется исходящий вызов на указанный в карточке номер
( ДЛЯ СОХРАНЕНИЯ ЗАПИСИ РАЗГОВОРА МОЖНО ЗВОНИТЬ ТОЛЬКО С УЖЕ СУЩЕСТВУЮЩЕЙ КАРТОЧКИ ЗАКАЗА )

- после окончания разговора запись прикрепляеться к данному заказу, сохранять заказ не обязательно
	![](/img/call_record.png "call_record")
( детальная настройка правил звонков настраивается в кабинете nextel https://my.nextel.com.ua/index.html#outscenarios )


#### Входящие звонки

- при входящем звонке в црм отобразиться всплывающее окошко, Ваш sip должен быть включен!
( детальная настройка правил звонков настраивается в кабинете nextel https://my.nextel.com.ua/index.html#inscenarios )

- когда ответите на звонок, Вы сможете сохранить данного клиента в црм, utm и номер телефона автоматически подставиться в новый заказ который нужно создавать ТОЛЬКО при нажатии на кнопку во всплывающем окне Сохранить заказ
* ![](/img/modal_in.png "modal_in")
 
* НЕ ЧЕРЕЗ ДОБАВИТЬ
* Данная функция сохранения работает только когда Вы находитесь в перечне заказов!



## АВТООБЗВОН
 - При успешной настройке модуля NEXTEL, в перечне заказов (1) у Вас появиться кнопка (2), которая открывает окно настроек автообзвона
* ![](/img/autodial.png "autodial")
* Основные настройки автообзвона создаются в кабинете nextel https://my.nextel.com.ua/index.html#autodial

- для манипуляции с номерами в автообзвоне - выделяем нужные заказы и открываем окно настроек автообзвона:
	![](/img/autodial_settings.png "autodial_settings")

- действия в поле "УПРАВЛЕНИЕ АВТООБЗВОНОМ" будут активны в зависимости от Статуса обзвона (на рис 3)
например: "Перезапуск обзвона" (на рис 8) будет доступен только для статуса "завершен"

- Пояснение по каждому пункту в окне настроек автообзвона:
	- № на рис 1 - при выборе автообзвона получаем статистику и состояние данного обзвона на рис (3, 4)
	№ на рис 2 - обновление данных для всех автообзвонов, если был добавлен новый автообзвон, в кабинете некстел, он добавиться в список выбора автообзвона
	№ на рис 3 - статус (текущее состояние) автообзвона, при действиях в поле "УПРАВЛЕНИЕ АВТООБЗВОНОМ" этот статус может изменяться
	№ на рис 4 - статистика.

	№ на рис 5 - в выбранных номерах будут отображаться номера с заказов которые выделели до открытия окна настроек автообзвона
	№ на рис 6 - действие добавления номеров в выбранный автообзвон ( по требованию nextel номера должны быть в международном формате ). Если будет ошибка хоть в 1м номере то не один номер не добавиться в автообзвон, в списке подсветяться невалидные номера
	№ на рис 7 - удаление номеров с автообзвона которые выделили. При удалении номеров все номера которые возможно удалить с данного автообзвона будут удалены, даже если в списке будет невалидный номер и будет ошибка
	№ на рис 8 - когда автообзвон завершен, его можно перезапустить, выбирая в списке статус номеров которые нужно обзвонить
	№ на рис 9, 10 - установка активного обзвона на паузу и снятие с нее соответственно
	№ на рис 11 - удаление всех номеров с обзвона, сброс статистики
	№ на рис 12 - завершение активного автообзвона




