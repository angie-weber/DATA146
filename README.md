# DATA146

## Python Review Exercises

### Exercise 1

years = list(data['year'].unique())

print(len(years), years)


### Exercise 2

max_pop = data['pop'].max()

loc_max_pop = data['pop'].idxmax()

print(data.loc[loc_max_pop])


### Exercise 3

target = data['continent'] == 'Europe'

Euro = data.loc[target]

year_sub = Euro['year'] == 1952

Euro_52 = Euro.loc[year_sub]

minimum_pop = Euro_52['pop'].idxmin()

print(minimum_pop)



country_min_pop = Euro_52.loc[684]

print(country_min_pop)



Ice_sub = Euro['country'] == 'Iceland'

Ice_sub = Euro.loc[Ice_sub]

year_07 = Ice_sub['year'] == 2007

year_07 = Ice_sub.loc[year_07]

print(year_07['pop'])
