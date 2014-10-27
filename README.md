# README File for the iGEM SUSTC-Shenzhen Team Wiki Framework

The framework that powers up the 2014 iGEM team SUSTC-Shenzhen team wiki.

Showcase:[SUSTC-Shenzhen](http://2014.igem.org/Team:SUSTC-Shenzhen)

## Introduction

The current implementation utilizes:

* The Bootstrap 3 HTML5 Framework  
* jQuery PJAX Library   
* normalize.css

## Usage
A normal page should include:
```
{{SUSTC-Shenzhen/removeStyles}}
{{SUSTC-Shenzhen/themeCss}}
{{:Team:SUSTC-Shenzhen/templates/nav-template}}

/* put the page body HERE */

{{SUSTC-Shenzhen/wiki-footer}}
{{SUSTC-Shenzhen/themeJs}}
```
### Document page (Frequently used)
You can use the WikiText format to write a page. However, a page must have the following format:
```
{{SUSTC-Shenzhen/removeStyles}}
{{SUSTC-Shenzhen/themeCss}}
{{:Team:SUSTC-Shenzhen/templates/nav-template}}

{{:Team:SUSTC-Shenzhen/templates/page-header|
       title=About the Project|
       subtitle=What is it?}}

{{SUSTC-Shenzhen/main-content-begin}}

/* Put WikiText here */

{{SUSTC-Shenzhen/main-content-end}}
{{SUSTC-Shenzhen/wiki-footer}}
{{SUSTC-Shenzhen/themeJs}}
```

### WikiText Essentials

#### 1. Typography
`=` stands for title, for example:
> =Heading 1=  
> ==Heading 2==  
> ===Heading 3===  
> ====Heading 4====    

This will render into:
> #Heading 1
##Heading 2
###Heading 3
####Heading 4

#### 2. Tables
Take this as a reference.
```
<html><div class="table-responsive"></html>

{|class="table"
! DNA concentration
! 0.5pg/ul
! 5pg/ul
! 10pg/ul
! 20pg/ul
! 50pg/ul
|-
!# of colonies
|10 - 20
|120 - 170
|280 - 360
|480 - 802
|500 - 1000+
|}

<html></div></html>
```
which renders into

| DNA concentration | 0.5pg/ul | 5pg/ul    | 10pg/ul   | 20pg/ul   | 50pg/ul     |
|-------------------|----------|-----------|-----------|-----------|-------------|
| # of colonies     | 10月20日 | 120 - 170 | 280 - 360 | 480 - 802 | 500 - 1000+ |

`!` stands for table headers
`|` stands for table cells
You can use [Table Generator](http://www.tablesgenerator.com/mediawiki_tables) to simplify the task of creating tables. Just copy and paste the table from __Excel__. __HERE YOU SHOULD NOTICE__ that if you are using __Word__ you have to first __COPY__ your table into excel of this will __NOT__ work!
After that, you __HAVE TO__ replace the `class="wikitable"` entity into `class="table"`.

#### 3. Images
Images can be a headache to upload, so do it wisely. This can be done in 3 steps:
1. Upload
2. Copy template
3. Edit template

The uploading process should be simple but __REMEMBER__ that you __SHOULD__ name the image file in `SUSTC-Shenzhen-<Your image title>.jpg` format, like `SUSTC-Shenzhen-AAAAA.jpg`.

Then you can use this template:
```
{{SUSTC-Image|<IMAGE PATH>|<IMAGE TITLE>}}
```
for example,
```
{{SUSTC-Image|wiki/images/5/5b/SUSTC-Shenzhen-20140728_21-30_BL21.jpg|BL21}}
```
The `<IMAGE PATH>` above can be obtained by clicking the __`Full Resolution(width x height)`__ link. Only the part starting with `wiki/` is needed.
The `<IMAGE TITLE>` can be whatever text you want.


