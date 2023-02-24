# Hotel-Reservation-Analysis---Data-Science-Project

**OBJECTIVE**

Analyze a dataset related to hotel reservation and draw business insights out of it

**Variables in the dataset**

1.IsCanceled  

2.LeadTime  

3.StaysInWeekendNights 

4.StaysInWeekNights

5.Adults  

6.Children 

7.Babies   

8.Meal 

9.Country     

10.MarketSegment  

11.IsRepeatedGuest   

12.PreviousCancellations

13.PreviousBookingsNotCanceled 

14.AssignedRoomType   

15.BookingChanges  

16.DepositType  

17.CustomerType  

18.RequiredCarParkingSpaces

19.TotalOfSpecialRequests

20.ReservedRoomType 
 
**There are 40060 observations in the dataframe and 20 variables**

![image](https://user-images.githubusercontent.com/100436462/221108394-30f41c50-8417-4633-8ac1-f467f2decf42.png)

**Using ggplot to generate histogram**

![image](https://user-images.githubusercontent.com/100436462/221108802-3d5cc248-fdb5-4da6-9a1a-43c981a5d446.png)

![image](https://user-images.githubusercontent.com/100436462/221109134-20fa3761-4453-48ee-99c4-64d96e681a27.png)

1.It can be seen that countires in bright yellow have lowest total number of cancellations and portion of the map in red have highest total number of cancellations

2.If we see the map carefully ,it can be seen that India,China ,Argentina have lowest total number of cancellations

3.Also we can see that Spain,Portugal ,France,Belgium ,Netherlands are few countries with highest total number of cancellations

# ASSOCATION RULE MINING

![image](https://user-images.githubusercontent.com/100436462/221109603-40ebc443-8d0c-4eb2-bd9c-97d9aedc9008.png)

1.We can see that rule 2 has a very high level of confidence which is 0.9894366. This measure defines the likeliness of occurrence of cancellation of booking  given that the meal type is FB 	FB	– Full	board	(breakfast,	lunch	and	dinner)		,market segment is groups, assignedRoom is A and customer type is transient

2.Rule 5 also has very high level of confidence which is 0.9894366 and it means that the likeliness of occurence of cancellation of booking is very high when the meal type is Full Board,assigned room type is A ,customer type is transient and there are  no changes in booking 

3.The support value of rule 2 is 0.007014478 which  gives an idea of how frequent an itemset is in all the transactions .In our case it means the ratio of all transactions when meal =FB ,marketSegment is Groups,assignedRoom =A , customer type is transient and booking got canceled out of total transactions is 0.007014478

4.The support value of rule 5 is 0.007014478 which  gives an idea of how frequent an itemset is in all the transactions .In our case it means the ratio of all transactions when meal =FB ,marketSegment is Groups,assignedRoom =A , customer type is transient,there were no changes in booking  and booking got canceled out of total transactions is 0.007014478

5.Lift is the rise in probability of having {Y} which means booking cancellation  on the cart with the knowledge of {X}, LHS  being present over the probability of having {Y} on the cart without any knowledge about presence of {X}.In rule 2 and 5 ,the lift is 3.563822 which is high compared to other rules and thus , we can say that when meal=FB,marketSegment=Groups,assignedRoom=A,customerType=Transient,bookingChanges=FALSE play an important role in booking cancellation


# SUPPORT VECTOR MACHINE

![image](https://user-images.githubusercontent.com/100436462/221109730-a5bf2533-b769-423b-97aa-ffdb86289fc6.png)

# DECISION TREE

![image](https://user-images.githubusercontent.com/100436462/221109973-af16423b-1868-4182-8c2c-b8a37053648c.png)



# Suggestions to the CEO 

1.Since ,Spain,Portugal ,France,Belgium ,Netherlands are few countries with highest total number of cancellations so the CEO should make friendly reservation policies  to reduce total number of cancellations in these European countries

2.The CEO should focus less on customers who select  meal=FB(Full Board), belong to marketSegment=Groups,are assignedRoom type A,                                    customerType is Transient ,bookingChanges=FALSE  as they do more number of cancellations and should focus more on guests who fall outside this category as they do less number of cancellations

3.We can see that the country with largest number of bookings is PRT which stands for Portugal and the total number of bookings is 63665 so the CEO should dedicate more resources for expansion of hotel bookings in Portugal

4.BB	– Bed	&	Breakfast is the most preferred type of breakfast when guests make booking so the CEO should focus on improvising this breakfast service

5.We also saw the type of payment method preferred by guests and No Deposit is the most preferred mode of payment while refundable is least preferred method of payment so the CEO should give offers in order to make refundable type of payment more attractive to guests

a.No	Deposit	– no	deposit	was	made such type of booking count is 38199

b.Non	Refund	– a	deposit	was	made	in	the	value	of	the	total	stay	cost and the count of these type of bookings is 1719

c.Refundable	– a	deposit	was	made	with	a	value	under	the	total	cost	of	stay and the count of these type of bookings is 142



```
