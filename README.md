# Python dictionaries: product price practice

Practice notebook from Virel Data Lab. I took one dictionary of product prices and answered a few basic questions with it, using only built-in Python (no pandas).

## Data

~~~python
products = {
    "Shoes": 5000,
    "Shirts": 3000,
    "Bags": 4000,
    "Watches": 2000,
    "Phones": 15000
}
~~~

## Questions

1. Display all product names

~~~python
print(products.keys())
# dict_keys(['Shoes', 'Shirts', 'Bags', 'Watches', 'Phones'])
~~~

2. Display all product prices

~~~python
print(products.values())
# dict_values([5000, 3000, 4000, 2000, 15000])
~~~

3. Total value of all products

~~~python
total_value = sum(products.values())
print("The total cost of all products is:", total_value)
# The total cost of all products is: 29000
~~~

4. Most expensive product

~~~python
maximum_product = max(products, key=products.get)
print("The most expensive product is:", maximum_product)
# The most expensive product is: Phones
~~~

5. Least expensive product

~~~python
minimum_product = min(products, key=products.get)
print("The least expensive product is:", minimum_product)
# The least expensive product is: Watches
~~~

6. Average product price

~~~python
average_price = sum(products.values()) / len(products)
print("The average price of all products is:", average_price)
# The average price of all products is: 5800.0
~~~

7. Products priced at 4000 and above

~~~python
for product, price in products.items():
    if price >= 4000:
        print(product)
# Shoes
# Bags
# Phones
~~~

## Notes

- `keys()` and `values()` return views, not lists, which is why the output says dict_keys and dict_values.
- `max(products, key=products.get)` gives back the product name, not the price. `min` works the same way.
- The last one uses `>=`, so Bags (exactly 4000) is included.

## Running it

Open `Data_Science_module_1.ipynb` in Google Colab or Jupyter and run the cells in order. Nothing to install.

Instagram: @virel_digital
