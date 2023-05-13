# PP_Boot_Security

Перенесите классы и зависимости из предыдущей задачи.
Создайте класс Role и свяжите User с ролями так, чтобы юзер мог иметь несколько ролей.
Имплементируйте модели Role и User интерфейсами GrantedAuthority и UserDetails соответственно. Измените настройку секьюрности с inMemory на userDetailService.
Все CRUD-операции и страницы для них должны быть доступны только пользователю с ролью admin по url: /admin/.
Пользователь с ролью user должен иметь доступ только к своей домашней странице /user, где выводятся его данные. Доступ к этой странице должен быть только у пользователей с ролью user и admin. Не забывайте про несколько ролей у пользователя!
Настройте logout с любой страницы с использованием возможностей thymeleaf.
Настройте LoginSuccessHandler так, чтобы админа после аутентификации направляло на страницу /admin, а юзера на его страницу /user.


Use this sql query in your database to correctly display roles during registration:

insert into roles (role_name) values ('ROLE_USER'), ('ROLE_ADMIN');
