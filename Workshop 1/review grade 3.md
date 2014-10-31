# Workshop1 - Domänmodellering

## Domänmodellering enligt problembeskrivning för betyg 3.
![Domänmodel](https://raw.githubusercontent.com/Grenmyr/Portfolio-Objektorienteradanalys/master/pics/grade3.JPG)

### Complementing text to domain model grade 3

The attribute /charge on Member object is derived from firstly a mandatory member fee
and a floating fee based on the amount of boat parking and the ParkingLot size.
/charge = member fee +(boat(s)*size).

We have added a Size object which handle compare about boats and a their size relative to
the ParkingLot of the boats to give a good matching from a size perspective. And since Member and
Boat has a association it is possible to make system match members boats as close as possible.

Object Role is created for the secretary to have a special role according to system requirements.
We choose a system using roles, we find it more suitable to add just one Member to a role.
The organization has one person for each special responsibility/role.

On object Payment there is an attribute called paymentOption which is an enum that represent different payment system from
third party solutions. We could have displayed on Model that our third party inherit from payment
but choose not to for understanding of Model.

Calender and Event is a separate model from the other model. We Assume a programmer knows that Event is date based and a calendar
also is so we did not model the attributes and relations. The requirement for secretary to handle booking of events is a system
solution that is accessed through the secretary Role from other model.

Note: In the diagram the association names are placed near the bottom instead of the center because of
limitations in the yUML drawing tool.
