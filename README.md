# Optimal Food Delivery Model
**by Wanqi Hu, Lezhen Qin, Xinran Wang**

*names by the alphabetical order of the last names*

**This is our final project for Math406: Mathematical Modeling**

## Introduction
In recent years, with the development of O2O (Online to Offline) e-commerce, China’s food delivery industry has burgeoned. Under the O2O pattern, the take-out orders go through the following process from generation to completion. First, consumers order food on third-party platforms like Meituan Takeout; The corresponding merchants accept the order and start food preparation. At the same time, the third-party platform allocates the delivery task and generates a route for its rider; When the rider receives and accepts the task, he starts from the site to pick up meals from the merchants. The food is ultimately delivered by the rider to the consumer’s location and the order is complete. The take-out delivery is different from expressage and other transportation by its immediacy and concentration on time. Especially, the influx of orders would experience a sharp increase during typical lunch and dinner rush hours, which requires an efficient distribution and optimization of the food delivery route of the rider. This is a core problem that the industry is urged to solve. In this project, we simulated the take-out delivery problem in Yushan city during noon rush hour from 11:00 am to 2:00 pm, and compared two allocation strategies: greedy strategy and K-means clustering. Greedy strategy attributes newly generated order to the nearest rider while K-means clustering matches the merchant-customer pair before attribution. Applying these strategies, we compare three major indexes of delivery efficiency: traveling distance, number of canceled orders, and number of time-out orders. Parameters involving deliver box capacity and penalty cost are adjusted to test the feasibility of the two strategies with respect to the above indexes under normal and rainy weather conditions. Our results reveal that both strategies have their advantages and disadvantages, and some index data (canceled number and time-out number) are largely dependent on parameters under different conditions.

## Model
### Greedy method
The basic principle of the greedy method is to assign newly generated orders to the nearest delivery staff who meets the vehicle capacity limit.

### Clustering method
We choose K-means clustering, one of the simplest and most popular machine learning algorithms as a clustering method. The working principle is to match the location of the merchant and the location of the customer of each order and convert the location of each order into a vector. Select the minimum value of the current number of unserviced orders and the number of available delivery staff as the number of clusters. Assign each cluster to the nearest available delivery staff. 
