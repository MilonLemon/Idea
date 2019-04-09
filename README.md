# Idea Project

(пояснения кому надо)  
Главный класс - **Application**
С помощью аннотации **@SpringBootApplication** подключаем контроллер GreetingController
В контроллере с помощью **@GetMapping**(название бина(раздел сайта)) указываем Spring-у, что необходимо объявить.  
Указывается метод, в котором есть параметры name = то, что передаем потом в html-шаблон ( {{name}} ), model - то, что добавляем на сайт в качестве переменных.  
Метод возвращает имя шаблона, который конструируется с соответствующим значением параметра
**@Controller** - тот, кто управляет Model и View.  
В данном примере за компоненту Model выступает объект model, за компоненту View - html файл (шаблон)

Как запускаем:

**1 вариант:**    
1.mvn package в консоли  
2.cd target  
3.java -jar Idea-1.0-SNAPSHOT.jar  
4.в браузере: http://localhost:8083/hello-world  

**2 вариант:**  
1.обязательно обновить зависимости (бывают проблемы): Maven Projects (справа раздел) - Значок "обновить"  
2.Edit Configurations - "+" - Application - Main class: (здесь указать Application)  
3.Собрать проект (Run)  
4.в браузере: http://localhost:8083/hello-world  

**Подключение к консоли БД:**  
http://localhost:8083/h2-console  
**JDBC URL**: jdbc:h2:mem:testdb  
**User Name**: girls;  
**Password**: 321;
