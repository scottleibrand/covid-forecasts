## COVID-19 Infections, Cases, and Deaths Forecasts

The model below [(and here)](https://my.causal.app/models/32376) shows the latest 7d average data on US COVID-19 cases and deaths, uses data on vaccinations from [another linked model](vaccine.html), and shows projections for future cases and deaths.

* The model’s assumptions are shown at the top (with descriptions), and you can edit them and it will immediately redraw the graphs to reflect the new assumptions.
* The model runs its calculations thousands of times, randomly selecting each input from the range provided.
* The results are presented as 90% uncertainty intervals, meaning that 90% of those thousands of runs fell within the shaded areas.
* The median outcome is shown as a central line.

The model assumes that the collective behavior of individuals and governments across the US will result in distancing and restrictions when cases are too high, and reopening and returns to previous normal levels of activity as case counts decline. The initial value for this “Cases per 100k target” is set at the range of case rates seen from peak to trough in summer 2020.

Additional details:
* The graphs at the bottom show the model’s predictions using data through January 12, and compare (backtest) those predictions against what has actually happened since then. These graphs are useful for checking whether the input assumptions are reasonable.
* Because COVID-19 epidemic growth and decay is an exponential process, this model (and reality) are very sensitive to a number of hard-to-estimate variables.

Please treat this model as a representation of how things might play out, and remember that the confidence intervals are wide for a reason.

Source data comes from [NYTimes](https://github.com/nytimes/covid-19-data) via [this Google sheet](https://docs.google.com/spreadsheets/d/11lgBxcW5jmxGV-osoFhnlAxgW6DzqZXzKdYuR43RbgA/edit).

{% include casesModel.html %}
