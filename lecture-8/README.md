## July 4 - Lecture 8 - SOLID, DRY

### Lecture overview:

- Clean Code
- Naming Conventions
- SOLID
- DRY

### Homework - Mega

|Description   |Screens   |
|---|---|
|Вход: <br/> - Содержит три поля ввода TextField (username, city, age) <br/> - City выбирается при помощи PickerView <br/> - Есть возможность добавления аватара |<img src="https://raw.githubusercontent.com/n17r-resources/ios/master/lecture-8/Screenshots/SignUp.png" width="600" height="600" /> |
|Еда: <br/> - Содержит список food компаний <br/> - Каждый Cell содержит в себе картинку, название компании, описание, средний чек и среднюю оценку <br/> - По умолчанию средний чек и средняя цена равны 0, они высчитываются основываясь на истории заказов <br/> - Список компаний получается с помощью `GET` запроса по данному URL `https://megaapi.herokuapp.com/api/food` <br/> <br/> Детальный экран:<br/> - Вверху отображается header картинка компании <br/> - Так же отображается средний чек и рейтинг (не кликабельны) <br/> - Содержит лист продуктов компании <br/> - Каждый Cell содержит картинку, цену и stepper (для увеличения кол-ва) и кнопку "Заказать" <br/> - При нажатии на кнопку "Заказать" выбранные продукты попадают в корзину и выходит Alert подтверждающий что выбор произведен успешно <br/> - Для получения продуктов определенной компании нужно сделать `GET` запрос по данному URL `https://megaapi.herokuapp.com/api/food/id/0` где вместо `0` указывается нужный id|<img src="https://raw.githubusercontent.com/n17r-resources/ios/master/lecture-8/Screenshots/Food.png" width="600" height="600" /> <br/> <img src="https://raw.githubusercontent.com/n17r-resources/ios/master/lecture-8/Screenshots/FoodDetailed.png" width="600" height="600" />| 
|Одежда: <br/> - Содержит список (можно и CollectionView) из clothes компаний <br/> - Список компаний получается с помощью `GET` запроса по данному URL `https://megaapi.herokuapp.com/api/cloth` <br/> <br/> Детальный экран: <br/> - Содержит Segment Control для сортировки типа товаров <br/> - Collection View для отображения предметов <br/> - Каждый Сell содержит картинку, название предмета и цену <br/> - Для получения продуктов определенной компании нужно сделать `GET` запрос по данному URL `https://megaapi.herokuapp.com/api/cloth/id/0` где вместо `0` указывается нужный id <br/> - При отсутствии каких либо элементов в категории нужно отобразить экран пустого состояния |<img src="https://raw.githubusercontent.com/n17r-resources/ios/master/lecture-8/Screenshots/Cloth.png" width="600" height="600" /> <br/> <img src="https://raw.githubusercontent.com/n17r-resources/ios/master/lecture-8/Screenshots/ClothDetailed.png" width="600" height="600" /> <img src="https://raw.githubusercontent.com/n17r-resources/ios/master/lecture-8/Screenshots/ClothEmpty.png" width="600" height="600" />|
|Экран выбора одежды: <br/> - Содержит карусель (carousel) из картинок которые можно листать, можно поставить одну картинку несколько раз <br/> - Содержит информацию по продукту (производитель, название продукта, описание производителя) <br/> - Выбор размера производится с помощью PickerView и в зависимости от `type`, если это `garment` то соответственно размеры должны быть `S, M, L, XL`. Если тип `shoes` то размеры должны быть `39, 40, 41`<br/>  |  <img src="https://raw.githubusercontent.com/n17r-resources/ios/master/lecture-8/Screenshots/ClothItem.png" width="600" height="600" /> |
|Корзина: <br/> - Содержит карточку с checkout информацией о собранном заказе <br/> - Содержимое заказа можно редактировать (удалять) <br/> - Высчитывается общая сумма заказа <br/> - При нажатии кнопки "Подтвердить" происходит проверка, если баланс пользователя больше чем сумма заказа то показывается Success экран, если нет то Failure экран с предложением удалить что-то из заказа <br/> |<img src="https://raw.githubusercontent.com/n17r-resources/ios/master/lecture-8/Screenshots/Basket.png" width="600" height="600" /> <br/> <img src="https://raw.githubusercontent.com/n17r-resources/ios/master/lecture-8/Screenshots/BasketSuccess.png" width="600" height="600" /> <br/> <img src="https://raw.githubusercontent.com/n17r-resources/ios/master/lecture-8/Screenshots/BasketError.png" width="600" height="600" />|
|Профиль: <br/> - Содержит базовую информацию о пользователе (username, city, age) <br/> - Есть кнопка "История заказов", при нажатии переходит на экран с историей заказов <br/> - При нажатии на кнопку "Выйти" возвращает на Login Page <br/> - Есть возможность смены аватара|<img src="https://raw.githubusercontent.com/n17r-resources/ios/master/lecture-8/Screenshots/Profile.png" width="600" height="600" /> <br/> <img src="https://raw.githubusercontent.com/n17r-resources/ios/master/lecture-8/Screenshots/History.png" width="600" height="600" />|