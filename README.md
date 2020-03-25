# Pediatric_Heart_Surgery_Mortality
An investigation on UNC Hospital's pediatric surgical data


Backgound
------------------
As the result of a recent New York Times expose, UNC Hospital recently suspended most of its complex
pediatric cardiovascular surgical procedures. 
Many hospitals participated in voluntary public reporting
through the Society for Thoracic Surgeons (STS) Congenital Heart Surgery Database and released their data over 4-year analytic time windows in each annual report.
While UNC did not participate in this program at the time of the expose, they eventually posted
2015-2018 mortality data online. 
Data
------------------
The data we have includes the number of pediatric (neonates + infants + children) surgical procedures
during the 2015-2018 reporting period and the number of deaths resulting from those procedures. 

The data contains the following variables.
• id: unique hospital identifier
• Hospital Name
• Procedure Type: overall (mortality for all procedures), STAT mortality category 1 (generally the
lowest risk procedures) through STAT mortality category 5 (generally the highest risk procedures)
• Observed deaths
• Total procedures (observed deaths/total procedures is the observed mortality rate)
• Expected mortality rate (this mortality rate is adjusted to reflect the individual case mix in the
procedure type of interest for the hospital of interest)

An important aspect of evaluating hospital performance in pediatric surgery is the consideration of the case
mix of each hospital. In particular, highly ranked programs may attract the more severely diseased
patients, leading to a more challenging group of procedures and higher mortality. In order to account for
the difficulty of the case mix, the data contain a hospital-specific expected mortality rate for procedures
in each of 5 categories, in which category 1 represents the simplest procedures (which should have the
lowest mortality), and category 5 represents the most challenging procedures associated with the highest
mortality. 
One common performance metric is the ratio of observed to expected (O to E) mortality rates, accompanied
by a 95% interval estimate. Ratios significantly higher than 1 indicate hospitals with significantly more
deaths than expected, while ratios < 1 indicate the better-performing hospitals. You can see in the UNC
data that mortality rates were quite high there relative to expectations for the more complex procedures.
The STS rates each hospital by providing a star rating as follows:
• one star: higher than expected operative mortality; the 95% confidence interval (CI) for a participant’s risk-adjusted O/E mortality ratio was entirely above the number 1
• two stars: as expected operative mortality; the 95% CI for a participant’s risk-adjusted O/E
mortality ratio overlapped with the number 1
• three stars: lower than expected operative mortality; the 95% CI for a participant’s risk-adjusted
O/E mortality ratio was entirely below the number 1
An alternative star method, used for adult procedures, awards three stars if the posterior probability
that the hospital’s mortality ratio exceeds the STS mean is 0.975 or greater, one star if the posterior
probability that the hospital’s mortality ratio exceeds the STS mean is 0.025 or lower, and two stars
otherwise.

