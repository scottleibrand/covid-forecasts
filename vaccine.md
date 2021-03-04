## COVID-19 Vaccination Forecasts

The model embedded below [(and here)](https://my.causal.app/models/28192) uses the latest data on US COVID-19 vaccine distribution and administration and generates projections for total vaccinations, vaccine availability, and vaccine immunity.

* The model’s assumptions are shown at the top (with descriptions), and you can edit them and it will immediately redraw the graphs to reflect the new assumptions.
* The model runs its calculations thousands of times, randomly selecting each input from the range provided.
* The results are presented as 90% uncertainty intervals, meaning that 90% of those thousands of runs fell within the shaded areas.
* The median outcome is shown as a central line.
* Two scenarios are shown by default. The one labeled "Default" uses the assumptions I consider most likely, which you can edit. The one labeled "Market Odds" uses the most plausible assumptions I could identify that are consistent with Polymarket's odds [on giving 100M first doses before 4/1](https://polymarket.com/market/will-100-million-people-have-received-a-dose-of-an-approved-covid-19-vaccine-in-the-us-by-april-1-2021).

The model assumes that:
* vaccine doses will be delivered by the manufacturers at the specified weekly rates for each month as they ramp up production.
* vaccination sites will administer the vaccine after a variable delay of days to weeks. 
* second doses will be given, on average, 3 to 5 weeks after the first dose.

Additional details:
* It models vaccine demand based on the "Vaccine hesitancy" and "Days to flat vax demand" assumptions: those determine how many people eventually get vaccinated, and how long it takes demand to tail off.
* It currently does not model any future EUAs or approvals beyond J&J’s. 
* Uncertainty about whether existing authorizations will be expanded to allow those <16 to be vaccinated is only indirectly represented in the wide range of assumptions for Vaccine hesitancy. It doesn’t yet directly model what will happen if/when a vaccine is authorized for children.

The outputs from this model are used in [this model forecasting COVID-19 infections, cases, and deaths](cases.html) based on this model's estimates of vaccine rollout, estimates of B.1.1.7 prevalence from Helix, and various editable assumptions.

Source data comes from [Youyang Gu's covid19-projections.com](https://covid19-projections.com), [Helix](https://github.com/myhelix/helix-covid19db), and [NYTimes](https://github.com/nytimes/covid-19-data) via [this Google sheet](https://docs.google.com/spreadsheets/d/11lgBxcW5jmxGV-osoFhnlAxgW6DzqZXzKdYuR43RbgA/edit).

{% include vaccineModel.html %}
