---

date: 2009-08-26 05:05:55+00:00
title: De-referencing climate claims
tags:
- climate change
- software
- sscc
- wind energy
---

[Our group](http://se.cs.toronto.edu) of software scientists, informaticians, and modeling experts at the University has been congregating weekly to discuss software science's role in {ameliorating|understanding|preventing|debunking} climate change. [Steve Easterbrook's](http://www.easterbrook.ca/steve/?p=799) been the inspiration.

[We have undertaken](http://se.cs.utoronto.ca/index.php/Modelling_solutions_to_climate_change) the[ challenge of modeling](http://www.easterbrook.ca/steve/?p=238) some of the claims and information used in climate change. We started out with wind renewables, specifically chaps 10/14/18/B in the Mackay book.

I found this figure interesting:

[caption id="" align="alignnone" width="395" caption="Predicted energy outputs, renewable energy sources"][![Predicted energy outputs, renewable energy sources](http://www.inference.phy.cam.ac.uk/withouthotair/c18/figure128.png)](http://www.inference.phy.cam.ac.uk/withouthotair/c18/page_107.shtml)[/caption]

It's from [Mackay, page 107,](http://www.inference.phy.cam.ac.uk/withouthotair/c18/page_107.shtml) and shows his estimates for renewable energy outputs, in kWh/day, in the first column, compared with four other sources. What I wanted to do was suss out the reasons for the discrepancies in the numbers. I've picked the offshore wind row, which he has as generating up to 48 kWh/d (32 deep, 16 shallow) vs 6.4, 4.6, and 21 kWh/d for other sources. That's a difference of between 2x and 10x, depending on source and whether you include deep offshore ('deep' is water deeper than 25 metres, not including floating generators). Mackay's numbers are derived from a series of [Fermi calculations](http://en.wikipedia.org/wiki/Fermi_problem) in his book.


### CAT report


The biggest number is 21kWh/d, which was included in the Centre for Alternative
Technology’s (CAT) “Island Britain” plan  -- Helweg-Larsen and Bull (2007). I found a copy of this online, and tried to figure out the genesis of this number.  The first sentence on page 85 gives 3,212 TWh/year as the potential amount of (offshore) wind energy, and estimates harnessing 14% of this by 2027. 14% of 3212 is 450, divided by 365 to give a daily figure, which is 1.23 TWh/day. MacKay gives his figures per person, so I used the population as of 2007, which is 61 million people, and divided by that, then multiplied by 106 (to change from Tera to kilo). Result is 20.16, which is close to the 21 kWh/day MacKay lists (probably due to rounding). Obviously the 2027 population of the UK will be much higher than 61 million, and I believe the figures used in the CAT report are only for Great Britain, which excludes a lot of offshore area around Ireland (and, I suppose, the Isle of Man, etc).

The key datum here is the 3,212 TWh/year estimate of potential wind energy offshore. That number comes from Department of Trade and Industry (Nov 2002) "[Future Offshore: A strategic framework for the offshore wind industry](http://webarchive.nationalarchives.gov.uk/+/http://www.berr.gov.uk/files/file22791.pdf)". In that report Table 2.2, page 26, summarizes the various wind energy potentials. This information is derived from a GIS that models water depth, wind speeds, etc. The report uses four strategic regions only, and omits water less than 5m deep, since there is likely to be greater conflicts closer to shore. However, the table calculates values for depths between 5 and 30 metres, and a second value for water between 30-50 m. The total energy production is then listed 3,213 TWh/year for all depths between 5-50m, within the four strategic regions. These regions are selected for location near the grid and also expanse of shallow water. They look comparatively small in size, so I suspect the totals are greatly underestimating the total potential (notwithstanding grid improvements to transfer the energy).

What is the cause of the difference between Mackay's 48kWh/day and CAT's 21kWh/day? One is due to this difference in the size of possible area. Mackay calculates the water depths, then arbitrarily takes 1/3 as usable (due to shipping etc).  Another is estimates of potential wind energy. He uses average power per square metre of 3 W/m2, while the CAT/DTI report presents no such estimate, but its calculations suggest they are using a factor of 12 W/m2. I cannot find their source for such a huge increase in the average power per unit area. Mackay, on page 60, lists the actual power for a running farm at 2.6 W/m2.

I think what the DTI/CAT report did was to place a '3MW' turbine every 500 metres, then multiply that density by the total area, to get total power capacity. I.e., for a one km2 unit, there would be nine turbines possible (using their 500m separation), for a power potential of 27W/m2. The DTI paper, on page 27, then assumes a 40% load factor (Mackay states industrial averages are nearer 30%). If we assume 10 turbines per km2 (not sure why 10 and not 9), we end up with the 12W/m2 figure they used. This is an unsafe assumption, however, as the real world data from Mackay seems to suggest. Certainly the factor of 4 improvement is highly suspect.


### Conclusions


It seems clear that this little exercise has pointed out some very interesting inconsistencies. Obviously, calculations for potential energy sources in twenty years will always be subject to some uncertainty -- who can say for sure what the possible results will be, or what 'unknown unknowns' will exist? Nonetheless, even for these simple analyses assumptions varied greatly -- available area, feasible sea depth, load factors, unit power.

To me, it seems clear that more detailed planning than these rough estimates should be performed. The DTI report, for example, seems to be a major policy statement of the UK government! And it isn't like the information is hard to gather, relative to other sciences. We could surely stick some anenometers out there to improve our knowledge of peak loads, evaluate current projects, perform some economic analysis like risk assessments, etc., in order to derive a more realistic, finer-grained model.

I would like to acknowledge Jon Udell, whose efforts in 'citizen e-democracy'  have been at the forefront for a long period of time. See, for example, his work [tracking down the sources](http://blog.jonudell.net/2009/07/12/the-civic-dashboard/) for crime statistics in his hometown. Too often the tidy figure quoted in a published study is the product of sloppiness and lazy research. And all too rarely is this figure fact-checked. But that is a (relatively) painless thing to do in the age of the Internet, and I think it behooves us all as citizens to do so.
