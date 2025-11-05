# Data Management Lab D2 Logbook

* For my definition of a pizza, I have used the following structure:
```xml
<pizza>
    <name>...</name>
    <base>...</base>
    <toppings>
        <topping>
            <name>...</name>
            <type>...</type>
        </topping>
        ...
    </toppings>
</pizza>
```
For example,
```xml
<pizza>
    <name>Margharita</name>
    <base>Classic</base>
    <toppings>
        <topping>
            <name>Mozzerella</name>
            <type>Cheese</type>
        </topping>
        <topping>
            <name>Tomato</name>
            <type>Fruit</type>
        </topping>
    </toppings>
</pizza>
```

* With the provided schema, it is not possible to have more than one cheese on the pizza. There may also be some conflicts if differrent pizzas have the same name.
* `//Cheese/text()` returns:
```
Text='Cheddar'
Text='Cheddar'
Text='Mozzarella'
```
* `//Pizza[last()-1]//Topping[1]` returns:
```
Element='<Topping>Pepperoni</Topping>'
```
As it is asking for the first topping of the penultimate pizza, which has pepperoni as its first listed topping.
* `//Cheese[text()="Mozzarella"]/..|Topping[text()="Pepperoni"]/../..` will return all pizzas with either mozzarella or pepperoni.
