1. Create entity Category with OneToMany Association
`php bin/console make:entit Category` {{execute}}

Choose: 
`
name
string
255
no
(enter to finish)
`

2. Prepare Product entity

`php bin/console make:entity` {{execute}}

Choose
```
Product
category
relation
Category
ManyToOne
no
yes
products
no
(enter to finish)
```

3. Run migrations

`php bin/console doctrine:migrations:diff` {{execute}}
`php bin/console doctrine:migrations:migrate` {{execute}}