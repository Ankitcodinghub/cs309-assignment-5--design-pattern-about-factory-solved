# cs309-assignment-5--design-pattern-about-factory-solved
**TO GET THIS SOLUTION VISIT:** [CS309 Assignment 5- Design Pattern About Factory Solved](https://www.ankitcodinghub.com/product/cs309-design-pattern-about-factory-and/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;116242&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS309 Assignment 5- Design Pattern About Factory Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Part 1 Abstract Factory

Experimental Objective

According to source code, learn what is the benefit of abstract factory, in which circumstance using abstract factory is better, and how to use abstract factory design pattern in different design layer.

Then exercise the basic usage of singleton design pattern.

Finally, exercise how to separate the dao layer from service layer in different ways.

Introduce of source code

1. Requirement introduction

There are two different kinds of databases in a project, the one is Mysql, and the other is SqlServer. In the project, there are two entity classes (Staff and Computer), and we need to do insert, update and delete operations of those two entities in both two databases respectively.

The original code is using simple factory design pattern. For example the ComputerFactory can return an instance of MysqlComputerDao or SqlServerComputerDao by passing different parameter. Accordingly, the client needs to generate two instances for two different factories, and then whether we can get correct instance of StaffDao and ComputerDao is determined by passing correct parameter.

In this tutorial, the task is that how can we get the instance of StaffDao and ComputerDao in a better way.

2. How to use it

After we get two instances, we can do a simple test:

3. Disadvantage analysis

What we want is to interact with only one database for one time, however if we pass a wrong parameter, we might interact the staff information with one database as the same time interact the computer information with another database

Abstract Factory

The abstract factory design pattern can provide a way to encapsulate a group of individual factories that have a common theme without specifying their concrete classes. Which means, the products created by only one concrete factory can not from different themes.

1. Class Diagram

Task 1

In abstractFactory package, please modify your code by using abstract factory design pattern in dao layer, and make sure that it can match the client.

Hints: You need to created two concrete classes including MysqlDaoFactory and

SqlServerDaoFactory to implements the interface DaoFactory

Refactoring Abstract Factory by Singleton

The Singleton Pattern ensures a class has only one instance and provides a global point of access to that instance.

1. Class Diagram

2. Sample code

or

Using reflection to separate two layers

If we want to switch database from one to another, we need to instantiate another concrete factory accordingly, in the process the source code needs to be changed. A better way is that, we can define the name of concrete factory into configure file, and then using reflection to instantiate an instance, so that we can switch the database only by changing the configure file instead of modifying the source code. In this case, defining two concrete factories are duplicated, only one is enough.

Complete all codes in DaoFactoryImpl , and modify it to be a singleton. Which concrete product it would be created is according to the data in properties file.

Hint:

How to create instance according to the String name of class?

Task 2

According to the promp above, in singleton package, please merge two concrete factories into one concrete factory ( DaoFactoryImpl ), and you need make sure that the instantiate process for StaffDao and ComputerDao is by reflection, and the class name of concrete factories are from resource.properties .

Modify your concrete factory ( DaoFactoryImpl ) to be a singleton.

Your code need to match the client.
