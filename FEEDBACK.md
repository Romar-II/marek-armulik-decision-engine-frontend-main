
Feedback for front and back-end

Biggest fix:

TASK 101 specifies that we need to display the highest amount according to chosen loan period.
In this case loan_form file compares for user chosen loan amount to the biggest available loan given by backend and displays the smaller amount.
This error is fixed

Smaller proposed fixes:

-Minimum displayed loan period on the slider is 6 months, should be 12, (fixed).

-Given its not binding calculator maybe its not that important but
there is an argument to be made to add some checks in the front end as well,
something that makes sure that backend response is indeed between 2 000 and 10 000 euros, same thing with loan period.

-When landing on page loan amount and period is set to 2500 and 36 months, these seem to be chosen for aesthetics,
which works for me, I would try to separate initial display variables from variables that we are actively checking information to improve readability

-LoanPeriod slider jumps by 6 months, if its standard to round up loans to periods divisible by 6 months then it makes sense,
if loans could be issued for any amount of months then slider can be changed, in slider.adaptive for loan period  
to display any amount of months between 12 and 60 months with:
_loanPeriod = ((newValue.floor()).round());