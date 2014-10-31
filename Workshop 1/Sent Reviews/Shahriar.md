# Assessment report
The report is great. The way you describe your work-process in detail helped us understand your domain model.

## Things to think about
The domain should be developed together with the domain expert (for example the Secretary) and it's for describing the organization.
It is important to not describe programming details since the domain expert can't relate to that. For example the domain expert
doesn't need to know the technical details behind the authentication.

In all your tasks you are mixing behavior logic into the associations. The associations should point out the relation between the
objects. A concrete example is in task 4 where a Member *registers* a New Boat which then *checks* the Calender and *assigns*
a Berth which *updates* the Member Fee. All this is a behavior flow rather than describing the relations between the objects.

We don't think you passed grade 3