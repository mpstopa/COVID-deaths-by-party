# COVID-deaths-by-party

This Jupyter notebook calculation takes the daily U.S. deaths due to COVID as compiled in the Johns Hopkins University Center for 
Systems Science and Engineering database (called JHU data within, here: https://github.com/CSSEGISandData), the statistics at the county level of the Hillary Clinton
versus Donald Trump vote percentage in the 2016 election, available here:
https://web.stanford.edu/~kjytay/courses/stats32-aut2018/Session%206/Elections_analysis.html
and the data on the political party affiliation of the 50 United States governors (tablualted within) and
caluclates the number of COVID-19-attributed deaths, by day and by county, for Clinton voters and Trump voters.

The calculation takes the JHU number of deaths in a given county (3146 total) on a given day 
(from January 22, 2020 to August 28, 2020) and multiplies them, by the percentage of Trump votes
and the percentage of Clinton votes to obtain, respectively, the number of "Republican" deaths
and the number of "Democrat" deaths.

It is understood of course that due to the large number of independent voters in the United States
as well as those who cross party lines these numbers are only a proxy for Republican and Democrat.
It is thus merely a convenient handle and the actual data is simply voted Clinton versus voted Trump.

An additional calculation is performed that attempts to assign responsibility to the COVID deaths.
Nevertheless, because the issue of political responsibility for the features of the pandemic are
so exceedingly complicated, no claim is made that this calculation has significance beyond the
parameters of the calculation, which are the following.

A control parameter for each county is calculated for each county based on two factors. First, the
party of the governor in the state in question is used to indicate state control. Then, a *majority*
of the Trump/Clinton vote in a given county is used to determine the "local control." For counties
having both state control and local control belonging to a singel party, all deaths are attributed 
to that party. In the case of a split between local and state control, 50% of deaths are attributed
to each party.

The results of these calculations are shown in figures 1 and 3. Figure 2 is similar to figure 3 except
that the state control (i.e. the party of the governor) are not included - only the county majority.
