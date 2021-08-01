# car_dealership

## Assignment
We were tasked to design an ERD for a car dealership based on given parameters and our understanding of how a car dealership works.
Our group collaborated to design and draw out the ERD, and then each individual created the database and filled it with values.

## Assumptions
Assumptions were made relating to the outward facing elements of the business. We decided to not tackle any pathways outside of
this particular dealership. For example, we knew dealerships probably interface with suppliers, both for parts and their parent company
for vehicles. We know that there are avenues of communication between the dealership and information databases (Car Fax, valuation databases),
and with state entities for licensing and titling. We decided to ignore those connections for the sake of this project.<br>

The one assumption we made in this ERD is the idea of an initial inspection. For the sake of our dealership, we made a decision that
each vehicle, new or used, would receive an initial inspection upon arrival. This would be obvious for used vehicles but we decided
to do this for new ones as well. Our reasoning was that if I own a Toyota dealership and get a shipment of cars in from Toyota, I would
want to verify the state of the vehicle because I now technically own that vehicle. As a dealership owner I don't want to blindly trust them.
Because of this, our ERD reflects that a car will have a one to many relationship with a service ticket because they will always be inspected
upon arrival.

## Relationships
Based on the nature of the ERD, all of our Primary Keys have a zero to many relationship to their Foreign Key in another table. This is because
they may appear on none or many of the rows in those tables. And mostly it is a one relationship the other way. So a car_id may show up in zero, one,
or many invoices, but an invoice will only ever have one car_id.<br>

The outlier to this is the relationship between part_id and serviceticket. Because we were told that a car being serviced "may or may not need parts",
and we know that a service ticket can't have many parts (because we don't know how to do that), then that relationship is zero to one. This means that each
serviceticket has either zero parts associated with it, or only one. But the part may show up in zero or many service tickets.

## Database
After building the tables in my database, I created a function for each table to add information. I then added five records to each table using these functions.
The functions did not include SERIAL values so that they could autopopulate, and I set a default for the timestamp so that it was not needed in the function.

## Lessons Learned
After completing this project it is very clear the importance of the planning stage in database building. Once the tables are setup and populated it is extremely
difficult to change things. So the more effort into the planning stage, and honestly the more minds involved, the better the process will be. It was really beneficial
to collaborate with people, be able to talk things out, and have different perspectives.
