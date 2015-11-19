# Apuntes de Computaci�n
#### Desarrollando caracter�sticas bajo el enfoque TDD en _Ruby on Rails_

C�digo de ejemplo del tutorial [Desarrollando caracter�sticas bajo el enfoque TDD en _Ruby on Rails_][1].

#### Pre-requisitos

* Ruby: MRI 2.2.3p173
* Rails 4.2.4
* gem 2.5.0
* bundle 1.10.6

Es recomendable el uso de [_rbenv_][2] con el plugin [_rb-build_][3] para la instalaci�n.

Se asume el uso de MySQL con _back-end_. Se puede utilizar cualquier otro _back-end_ soportado por **_ActiveRecord_** con los cambios necesarios en _config/database.yml_.

El correcto funcionamiento del ejemplo no est� garantizado si se usan distintas versiones de las indicadas.

#### Instalaci�n

Ejecutar en el directorio ra�z del proyecto:
```sh
$ git clone https://github.com/joseraf86/dictionary_tdd.git
$ bundle install
$ bundle exec rake db:setup
$ bundle exec rake test -v
```

Editar _config/database.yml_ y _config/secrets.yml_ con los datos del usuario de base de datos.

Ejecutar el servidor de pruebas:
```sh
$ bundle exec rails s
```

Comprobar la aplicaci�n en:

[http://127.0.0.1:3000/words/learn][3]

Deber�a generarse una palabra en ingl�s aleatoriamente y su respectiva traducci�n al espa�ol.

#### Seguir los 15 pasos

Ver detalles en [Desarrollando caracter�sticas bajo el enfoque TDD en _Ruby on Rails_][1].

1. Crear una nueva aplicaci�n _Rails_
2. Configurar la base de datos
3. Crear el modelo _Word_ con el correspondiente _test_ unitario
4. Programar el _test_ unitario de la clase _Word_
5. Ejecutar la migraci�n _db/migrate/xxxxxxxxxxxxxx_create_words.rb_
6. Crear los fixtures y el _test_ para el m�todo _Word.random_
7. Implementar el m�todo _Word.random_
8. Generar el controlador Words con la acci�n _learn_
9. Escribir un _test_ para la acci�n _learn_
10. Hacer que el _test_ pase
11. Reescribir el _test_ en  _test/controllers/words_controller_test.rb_
12. Codificar  la implementaci�n
13. Verificar que la palabra es mostrada
14. Implementar la vista de la acci�n _learn_
15. Verificaci�n manual

#### Lecturas recomendadas

* [15 _TDD steps to create a Rails application_][4] **(Fuente original/_Original source_: _Thoughts on Software_ - Andrzej Krzywda)**
* [_A Guide to Testing Rails Applications_][5] **(Gu�a oficial de _Rails_/_Official Rails guide_)**
* [_Red-Green-Refactor_][6] **(_Blog_ personal de James Shore/_James Shore's personal blog_)**
* [_Introduction to Test Driven Development_ (TDD)][7] **(_Agile Data_ por Scott Ambler/_Agile Data by Scott Ambler_)**

#### Contacto
joserafaelguevara@gmail.com

[//]: # (REFERENCIAS)
[1]: <https://joserafaelguevara.wordpress.com/2015/11/12/%desarrollando-caracteristicas-bajo-el-enfoque-tdd-en-ruby-on-rails>
[2]: <https://github.com/sstephenson/rbenv>
[3]: <https://github.com/sstephenson/ruby-build>
[4]: <http://andrzejonsoftware.blogspot.com.es/2007/05/and-some-more-tdd-steps-with-rails.html>
[5]: <http://guides.rubyonrails.org/testing.html>
[6]: <http://www.jamesshore.com/Blog/Red-Green-Refactor.html>
[7]: <http://agiledata.org/essays/tdd.html>
