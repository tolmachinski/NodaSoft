# NodaSoft

Здравствуйте. 
Бегло прошелся по одному из файлов и написал комменты в тех местах,где я бы хотел внести правки.

Несколько правок по другим параметрам:
1. Валидация:
  Вы преобразуете $data['resellerId'] и $data['notificationType'] в целые числа, не проверяя, действительно ли они числовые. 
  Функция проверки, допустим, как is_numeric(), или другие проверки валидации могут это исправить.
2. Эксепшены:
  Не стоит раскрывать данные при выбросе эксепшена, так же,как и структуры бд. 
3. Чистка:
  Есть возможность sql инъекции,так как данные пользователя не обработаны до употребления их в запросах.
4. Константы:
   Считаю важным описывать маг методы любым доступным способом (CHANGE_RETURN_STATUS).
5. Обработка мэйла:
  Лучше использовать какую-то библиотеку для обработки и работы с данными по емейлу,либо как-то скрывать их.
6. Ошибки:
  Лучше отключить отчеты об ошибках, чтобы не раскрывать данные. display_errors = off .
  
