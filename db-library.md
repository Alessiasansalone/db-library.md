# DB library

table: books

- id \ (BIG)INT \ PK \ AI(autoincremento [di default anche unique]) \ NOTNULL 
- title \ VARCHAR(80) [esiste anche CHART, ma occupa sempre e solo il numero di caratteri indicato fra parentesi] \ NOTNULL

- plot \ TEXT \ NULL | NULL
- price \ DECIMAL (6,2) \ NULL | NULL
- year \ YEAR \ NULL | NULL

- category \ (VARCHAR)?

- author \ (VARCHAR) - VARCHAR \ NULL | NOTNULL
- ISBN \ (MEDIUMINT) - CHAR(13) \ NULL | NOTNULL UNIQUE
- edition \ (SMALLINT) - TINYINT() \ NULL | 
- pages \ (MEDIUMINT) - SMALLINT \ NULL |
- publisher \ (VARCHAR) - VARCHAR(80) \ NULL | NULL
- condition \ (TEXT) - VARCHAR(80) \ NULL | NULL DEFAULT('new' / 'second hand')
- language \ (VARCHAR) - VARCHAR (5) \ NULL | NOTNULL
- notes \ (MEDIUMTEXT) - TEXT \ NULL | NULL


table: loans

- id
- book_id UNSIGNED BIGINT FK
- user_id UNSIGNED BIGINT FK
- starter_date DATE
- end_date DATE


table: users

- id
- books_on_loan
- lent_book