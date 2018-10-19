# Veterinarian's Office Challenge

You have just been hired by Happy Paws & Claws, your neighborhood veterinarian's office to organize their information. Your 3 classes are `Animal`, `Vet`, and `Appointment`

An animal has many appointments, and an appointment belongs to an Animal.
A vet has many appointments, and an appointment belongs to a vet.

Along with the necessary relations between our classes, the following information is stored as well:

An animal has a name (string), age (integer), weight (integer), and if they are vaccinated (boolean). 
A veterinarian has a name (string), and years experience (integer). 
An an appointment has a date (string) and a cost (float) (date strings should be written "MM/DD/YYYY").

As always, make sure to sketch out your domain and think about the single source of truth for your data.


We've provided you with a console that you can use to test your code. To enter a console session, run `ruby tools/console.rb`. You must run this from this assignment's root directory, not from inside the tools directory.

## Deliverables

Implement all of the methods described below

### `Animal`

+ `Animal.all`
  + returns all of the Animals
+ `Animal#appointments`
  + returns all the `Appointment` instances associated with this instance of `Animal`
+ `Animal#vets`
  + returns an array of `Veterinarian` names associated with this instance of `Animal`
+ `Animal#make_appointment(veterinarian, date, cost)`
  + given a veterinarian, date, and cost, creates a new `Appointment` instance and associates it with this `Animal`
+ `Animal.average_age`
  + Calculates the average age of all the animals in the `Animal` class
+ `Animal.too_heavy_to_lift`
  + Returns an array of all the `Animal`s who weigh over 100 pounds
+ `Animal.percent_vaccinated`
  + Returns the percentage of all `Animal` instances that are percent_vaccinated
+ `Animal.longest_name`
  + Returns the `Animal` with the longest name
+ `Animal#appointment_total_cost`
  + Returns the total cost of all `Appointment`s for this instance of `Animal`

### `Appointment`

+ `Appointment.all`
  + returns an array of all `Appointment`s
+ `Appointment#Animal`
  + returns the Animal associated with this `Appointment`
+ `Appointment#Veterinarian`
  + returns the Veterinarian associated with this `Appointment`
+ `Appointment.most_expensive`
  + Returns the `Animal` name and `Veterinarian` name for the most expensive `Appointment`
+ `Appointment.find_appointments_by_date(date)`
  + Given a date string, returns all the appointments for that particular day
+ `Appointment.vet_available?(veterinarian, date)`
  + Given a veterinarian and a date, check to see if that vet has any appointments on that day


### `Veterinarian`

+ `Veterinarian.all`
  + returns an array of all `Veterinarian`s
+ `Veterinarian#appointments`
  + returns an array of all the `Appointment` instances that have this veterinarian
+ `Veterinarian#animals`
  + returns an array of all of the `Animal`s with this `Veterinarian` instance in their queue
+ `Veterinarian#average_patient_age`
  + returns the average age of all the `Animal`s who have `Appointment`s with this veterinarian
+ `Veterinarian.most_years_practiced`
  + returns the instance of `Veterinarian` with the highest number of years practicing
+ `Veterinarian#heaviest_patient`
  + returns the name of the `Animal` with the highest weight that has an `Appointment` with this instance of `Veterinarian`
+ `Veterinarian#vaccinate(Animal)`
  + Takes an `Animal` instance and changes it's vaccination status from `false` to `true`
+ `Veterinarian#all_vaccinated`
  + Checks to see if all of the `Animal`s that have appointments with this `Veterinarian` are vaccinated
