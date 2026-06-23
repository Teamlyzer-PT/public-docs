![Version badge](https://img.shields.io/badge/Version-1.0.2-blue.svg?maxAge=2592000)

**CSV import template**
=======================

This template aims to map the following interface for mass import from external sources: 
https://pt.teamlyzer.com/users/salary-review

Table of contents
=================

  * [CSV import template](#csv-import-template)
  * [Table of contents](#table-of-contents)
  * [Introduction](#introduction)
  * [Columns](#columns)
    * [id](#id)
    * [user_id](#user_id)
    * [role](#role)
    * [ts](#ts)
    * [last_year](#last_year)
    * [size](#size)
    * [industry_id](#industry_id)
    * [hide_company](#hide_company)
    * [senior_junior](#senior_junior)
    * [salary_range](#salary_range)
    * [salary_range_offer_min](#salary_range_offer_min)
    * [salary_range_offer_max](#salary_range_offer_max)
    * [approved](#approved)
    * [new_moderated](#new_moderated)
    * [moderated_by](#moderated_by)
    * [user_ip](#user_ip)
    * [user_hash](#user_hash)
    * [cookie_token_fg](#cookie_token_fg)
    * [company_id](#company_id)
    * [company_location_id](#company_location_id)
    * [salary_ac](#salary_ac)
    * [tag](#tag)
    
**Introduction**
================

There are salary submissions where the user specifies the company (1) and where they do not (2).

Please note:

- (1) If you specify a company. Set `hide_company` (column H) to `FALSE` and add `company_id` (column S).
- (2)  If you do not specify a company. Set `hide_company` (column H) to `TRUE` and add `industry_id` (column G) and `size` (column F). 

**Columns**
===========

id
--

* **Description** 
`Mandatory. Incremental order starting at 1.`

* **Required** 
`id=[integer]`

user_id
-------

* **Description** 
`Mandatory. Your user_id.`

* **Required** 
`id=[integer]`

role
----

* **Description** 
`Mandatory. Map with the role of each salary.`

* **Required** 
`id=[integer]`

* **Options** 
 
    | Id | Description |
    | ------ | ------ |
    | 1 | Programador de software |
    | 2 | Programador Web e de multimédia |
    | 3 | Programador de aplicações mobile |
    | 4 | Outros analistas e programadores, de software e aplicações |
    | 5 |  Especialista em base de dados |
    | 6 |  Administrador de sistemas |
    | 7 |  Especialista em redes informáticas |
    | 8 |  Outros especialistas em base de dados e redes |
    | 9 |  Engenheiro electrotécnico |
    | 10 |  Engenheiro electrónico |
    | 11 |  Engenheiro de telecomunicações |
    | 12 |  Designer, gráfico ou de comunicação e multimédia |
    | 13 |  Designer de jogos |
    | 16 |  Designer de produto industrial ou de equipamento |
    | 17 |  Artista 2d/3d |
    | 18 |  Técnico operador das TIC |    
    | 19 |  Técnico de help desk |
    | 20 |  Técnico de telecomunicações |
    | 21 |  Técnico de suporte |
    | 22 |  Gestor de Produto |
    | 23 |  Gestor de Projeto |
    | 24 |  Formador em tecnologias de informação |

ts
--

* **Description** 
`Mandatory. Date of this file.`

* **Required** 
`string=[2021-09-22 14:05:29+00]`

last_year
---------

* **Description** 
`Mandatory. Salary year. E.g: 2022.`

* **Required** 
`id=[integer]`

size
----

* **Description** 
`Not mandatory, but recommended if hide_company = TRUE.`

* **Required** 
`string=[11-50]`

* **Options** 

    | Value | Description |
    | ------ | ------ |
    | 1-10  | 1 to 10  |
    | 11-50 | 11 to 50 |
    | 51-200 | 51 to 200 |
    | 201-500 | 201 to 500 |
    | 501-1000 | 501 to 1000 |
    | 1001-5000 | 1001 to 5000 |
    | 5001-10000 | 5001 to 10000 |
    | +10000 | +10000 |

hide_company
------------

* **Description** 
`Mandatory. If user reveal the company set FALSE. If not set TRUE.`

* **Required** 
`boolean=[TRUE]`

industry_id
-----------

* **Description** 
`Mandatory if hide_company = TRUE`

* **Required** 
`id=[integer]`

* **Options** 

    | Id | Description |
    | ------ | ------ |
    | 1 | Banca & Serviços Financeiros  |
    | 2 | Ciência & Investigação |
    | 3 | Consultoria & Outsourcing IT |
    | 4 | Formação & Educação |
    | 5 | Hardware & Produtos Eletrónicos |
    | 6 | Indústria & Serviços |
    | 7 | Publicidade, Multimédia & Videojogos |
    | 8 | Software House & Internet |
    | 9 | Tecnologia da Informação |
    | 10 |  Telecomunicações & Eletrotécnica |
        
senior_junior
-------------

* **Description** 
`Mandatory. Sénior or Júnior.`

* **Required** 
`string=[Sénior]`

* **Options** 

    | Value | Description |
    | ------ | ------ |
    | Sénior | >= 3 years of experience |
    | Júnior | < 3 years of experience |

salary_range
------------

* **Description** 
`Do not fill`

salary_range_offer_min
----------------------

* **Description** 
`Mandatory. Min 400. Max 6200. Youd should sum the gross salary plus allowences (If any). The difference between salary_range_offer_min and salary_range_offer_max must be always 200€`. 

* **Required** 
`integer=[1000]`

* **Options** 

    | Value | Description |
    | ------ | ------ |
    | 400 | 400€ |
    | 500 | 500€ |
    | 600 | 600€ |  
    | 700 | 700€ |  
    | 800 | 800€ |  
    | 900 | 900€ |  
    | 1000 | 1000€ | 
    | 1100 | 1100€ |
    | 1200 | 1200€ |  

    | Value | Description | 
    | ------ | ------ |
    | 1400 | 1400€ |  
    | 1500 | 1500€ |  
    | 1600 | 1600€ |
    | 1700 | 1700€ |
    | 1800 | 1800€ |
    | 1900 | 1900€ |
    | 2000 | 2000€ |
    | 2100 | 2100€ |
    | 2200 | 2200€ |

    | Value | Description | 
    | ------ | ------ |
    | 2400 | 2400€ |
    | 2500 | 2500€ |
    | 2600 | 2600€ |
    | 2700 | 2700€ |
    | 2800 | 2800€ |
    | 2900 | 2900€ |
    | 3000 | 3000€ |
    | 3100 | 3100€ |
    | 3200 | 3200€ |
    
    | Id | Description | 
    | ------ | ------ |
    | 3400 | 3400€ |
    | 3500 | 3500€ |
    | 3600 | 3600€ |
    | 3700 | 3700€ |
    | 3800 | 3800€ |
    | 3900 | 3900€ |
    | 4000 | 4000€ |
    | 4100 | 4100€ |
    | 4200 | 4200€ |
    
    | Id | Description | 
    | ------ | ------ |
    | 4400 | 4400€ |
    | 4500 | 4500€ |
    | 4600 | 4600€ |
    | 4700 | 4700€ |
    | 4800 | 4800€ |
    | 4900 | 4900€ |
    | 5000 | 5000€ |
    | 5100 | 5100€ |
    | 5200 | 5200€ |
    
    | Id | Description | 
    | ------ | ------ |
    | 5400 | 5400€ |
    | 5500 | 5500€ |
    | 5600 | 5600€ |
    | 5700 | 5700€ |
    | 5800 | 5800€ |
    | 5900 | 5900€ |
    | 6000 | 6000€ |
    | 6100 | 6100€ |
    | 6200 | 6200€ |

    | Id | Description |
    | ------ | ------ |
    | 6400 | 6400€ |
    | 6500 | 6500€ |
    | 6600 | 6600€ |
    | 6700 | 6700€ |
    | 6800 | 6800€ |
    | 6900 | 6900€ |
    | 7000 | 7000€ |
    | 7100 | 7100€ |
    | 7200 | 7200€ |
    
salary_range_offer_max
----------------------

* **Description** 
`Mandatory. Min 600. Max 6400 Youd should sum the gross salary plus allowences (If any)`.

* **Required** 
`integer=[1200]`

* **Options** 

    | Value | Description |
    | ------ | ------ |
    | 600 | 600€ |
    | 700 | 700€ |
    | 800 | 800€ |  
    | 900 | 900€ |  
    | 1000 | 1000€ |  
    | 1100 | 1100€ |  
    | 1200 | 1200€ | 
    | 1300 | 1300€ |
    | 1400 | 1400€ |  

    | Id | Description | 
    | ------ | ------ |
    | 1600 | 1600€ |  
    | 1700 | 1700€ |  
    | 1800 | 1800€ |
    | 1900 | 1900€ |
    | 2000 | 2000€ |
    | 2100 | 2100€ |
    | 2200 | 2200€ |
    | 2300 | 2300€ |
    | 2400 | 2400€ |

    | Id | Description | 
    | ------ | ------ |
    | 2600 | 2600€ |
    | 2700 | 2700€ |
    | 2800 | 2800€ |
    | 2900 | 2900€ |
    | 3000 | 3000€ |
    | 3100 | 3100€ |
    | 3200 | 3200€ |
    | 3300 | 3300€ |
    | 3400 | 3400€ |
    
    | Id | Description | 
    | ------ | ------ |
    | 3600 | 3600€ |
    | 3700 | 3700€ |
    | 3800 | 3800€ |
    | 3900 | 3900€ |
    | 4000 | 4000€ |
    | 4100 | 4100€ |
    | 4200 | 4200€ |
    | 4300 | 4300€ |
    | 4400 | 4400€ |
    
    | Id | Description | 
    | ------ | ------ |
    | 4600 | 4600€ |
    | 4700 | 4700€ |
    | 4800 | 4800€ |
    | 4900 | 4900€ |
    | 5000 | 5000€ |
    | 5100 | 5100€ |
    | 5200 | 5200€ |
    | 5300 | 5300€ |
    | 5400 | 5400€ |
    
    | Id | Description | 
    | ------ | ------ |
    | 5600 | 5600€ |
    | 5700 | 5700€ |
    | 5800 | 5800€ |
    | 5900 | 5900€ |
    | 6000 | 6000€ |
    | 6100 | 6100€ |
    | 6200 | 6200€ |
    | 6300 | 6300€ |
    | 6400 | 6400€ |

    | Id | Description |
    | ------ | ------ |
    | 6600 | 6600€ |
    | 6700 | 6700€ |
    | 6800 | 6800€ |
    | 6900 | 6900€ |
    | 7000 | 7000€ |
    | 7100 | 7100€ |
    | 7200 | 7200€ |
    | 7300 | 7300€ |
    | 7400 | 7400€ |

approved
--------

* **Description** 
`Mandatory TRUE`.

* **Required** 
`boolean=[True]`

new_moderated	
-------------

* **Description** 
`Do not fill`

moderated_by	
------------

* **Description** 
`Do not fill`

user_ip	
-------

* **Description** 
`Do not fill`

user_hash	
---------

* **Description** 
`Do not fill`

cookie_token_fg
---------------

* **Description** 
`Do not fill`

company_id 
----------

* **Description** 
`Mandatory if hide_company = FALSE`

* **Source** 
https://docs.google.com/spreadsheets/d/1gwXfth3pg4HuJTYtPa0t18_KOP6QGVWp5IupVJknvSE

* **Required** 
`id=[integer]`

company_location_id
-------------------

* **Description** 
`Mandatory. Company location regarding each salary`

* **Required** 
`id=[integer]`

* **Options** 

    | Id | Description |
    | ------ | ------ |
    | 1 | Lisboa |
    | 2 | Porto |
    | 3 |  Braga |  
    | 4 |  Setúbal |  
    | 5 |  Aveiro |  
    | 6 |  Faro |  
    | 7 |  Leiria | 
    | 8 |  Coimbra |
    | 9 |  Santarém  |  
    | 10 |  Viseu |  
    | 11 |  Madeira |  
    | 12 |  Açores  |  
    | 13 |  Viana do Castelo |  
    | 14 |  Vila Real |  
    | 15 |  Castelo Branco |  
    | 16 |  Évora |  
    | 17 |  Guarda |  
    | 18 |  Beja |  
    | 19 |  Bragança |  
    | 20 |  Portalegre |  
            
salary_ac
---------

* **Description** 
` Mandatory. Percentage of allowances. E.g. Total salary of 800€ + 200€ in allowances = 1000€. You sould fill with 20%. 0 if no allowances.` 

* **Required** 
`integer=[20]`

