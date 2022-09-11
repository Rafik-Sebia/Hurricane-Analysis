# names of hurricanes
names = ['Cuba I', 'San Felipe II Okeechobee', 'Bahamas', 'Cuba II', 'CubaBrownsville', 'Tampico', 'Labor Day', 'New England', 'Carol', 'Janet', 'Carla', 'Hattie', 'Beulah', 'Camille', 'Edith', 'Anita', 'David', 'Allen', 'Gilbert', 'Hugo', 'Andrew', 'Mitch', 'Isabel', 'Ivan', 'Emily', 'Katrina', 'Rita', 'Wilma', 'Dean', 'Felix', 'Matthew', 'Irma', 'Maria', 'Michael']

# months of hurricanes
months = ['October', 'September', 'September', 'November', 'August', 'September', 'September', 'September', 'September', 'September', 'September', 'October', 'September', 'August', 'September', 'September', 'August', 'August', 'September', 'September', 'August', 'October', 'September', 'September', 'July', 'August', 'September', 'October', 'August', 'September', 'October', 'September', 'September', 'October']

# years of hurricanes
years = [1924, 1928, 1932, 1932, 1933, 1933, 1935, 1938, 1953, 1955, 1961, 1961, 1967, 1969, 1971, 1977, 1979, 1980, 1988, 1989, 1992, 1998, 2003, 2004, 2005, 2005, 2005, 2005, 2007, 2007, 2016, 2017, 2017, 2018]

# maximum sustained winds (mph) of hurricanes
max_sustained_winds = [165, 160, 160, 175, 160, 160, 185, 160, 160, 175, 175, 160, 160, 175, 160, 175, 175, 190, 185, 160, 175, 180, 165, 165, 160, 175, 180, 185, 175, 175, 165, 180, 175, 160]

# areas affected by each hurricane
areas_affected = [['Central America', 'Mexico', 'Cuba', 'Florida', 'The Bahamas'], ['Lesser Antilles', 'The Bahamas', 'United States East Coast', 'Atlantic Canada'], ['The Bahamas', 'Northeastern United States'], ['Lesser Antilles', 'Jamaica', 'Cayman Islands', 'Cuba', 'The Bahamas', 'Bermuda'], ['The Bahamas', 'Cuba', 'Florida', 'Texas', 'Tamaulipas'], ['Jamaica', 'Yucatn Peninsula'], ['The Bahamas', 'Florida', 'Georgia', 'The Carolinas', 'Virginia'], ['Southeastern United States', 'Northeastern United States', 'Southwestern Quebec'], ['Bermuda', 'New England', 'Atlantic Canada'], ['Lesser Antilles', 'Central America'], ['Texas', 'Louisiana', 'Midwestern United States'], ['Central America'], ['The Caribbean', 'Mexico', 'Texas'], ['Cuba', 'United States Gulf Coast'], ['The Caribbean', 'Central America', 'Mexico', 'United States Gulf Coast'], ['Mexico'], ['The Caribbean', 'United States East coast'], ['The Caribbean', 'Yucatn Peninsula', 'Mexico', 'South Texas'], ['Jamaica', 'Venezuela', 'Central America', 'Hispaniola', 'Mexico'], ['The Caribbean', 'United States East Coast'], ['The Bahamas', 'Florida', 'United States Gulf Coast'], ['Central America', 'Yucatn Peninsula', 'South Florida'], ['Greater Antilles', 'Bahamas', 'Eastern United States', 'Ontario'], ['The Caribbean', 'Venezuela', 'United States Gulf Coast'], ['Windward Islands', 'Jamaica', 'Mexico', 'Texas'], ['Bahamas', 'United States Gulf Coast'], ['Cuba', 'United States Gulf Coast'], ['Greater Antilles', 'Central America', 'Florida'], ['The Caribbean', 'Central America'], ['Nicaragua', 'Honduras'], ['Antilles', 'Venezuela', 'Colombia', 'United States East Coast', 'Atlantic Canada'], ['Cape Verde', 'The Caribbean', 'British Virgin Islands', 'U.S. Virgin Islands', 'Cuba', 'Florida'], ['Lesser Antilles', 'Virgin Islands', 'Puerto Rico', 'Dominican Republic', 'Turks and Caicos Islands'], ['Central America', 'United States Gulf Coast (especially Florida Panhandle)']]

# damages (USD($)) of hurricanes
damages = ['Damages not recorded', '100M', 'Damages not recorded', '40M', '27.9M', '5M', 'Damages not recorded', '306M', '2M', '65.8M', '326M', '60.3M', '208M', '1.42B', '25.4M', 'Damages not recorded', '1.54B', '1.24B', '7.1B', '10B', '26.5B', '6.2B', '5.37B', '23.3B', '1.01B', '125B', '12B', '29.4B', '1.76B', '720M', '15.1B', '64.8B', '91.6B', '25.1B']

# deaths for each hurricane
deaths = [90,4000,16,3103,179,184,408,682,5,1023,43,319,688,259,37,11,2068,269,318,107,65,19325,51,124,17,1836,125,87,45,133,603,138,3057,74]


# 1 Write a function that returns a new list of updated damages where the recorded data is converted to float values and the missing data is retained as "Damages not recorded".


updated_damages = []

def updating_damages(damage):
  # Update Recorded Damages
  conversion = {"M": 1000000,
                "B": 1000000000}

  x = 0
  for damage in damages:
    if "M" in damage:
      updated_damages.append(float(damages[x].strip("M"))*conversion["M"])
    elif "B" in damage:
      updated_damages.append(float(damages[x].strip("B"))*conversion["B"])
    else:
      updated_damages.append(damages[x])
    x += 1
  return updated_damages
print(updating_damages(damages))


# 2 Write a function that constructs a dictionary made out of the lists, where the keys of the dictionary are the names of the hurricanes, and the values are dictionaries themselves containing a key for each piece of data (Name, Month, Year,Max Sustained Wind, Areas Affected, Damage, Death) about the hurricane.


def hurricane_dict(names, months, years, max_sustained_winds, areas_affected, updated_damages, deaths):
  hurricane = {}
  for index in range(0, len(names)):
    hurricane[names[index]] = {"Name": names[index],
                           "Month": months[index],
                           "Year": years[index],
                        "Max Sustained Wind": max_sustained_winds[index],
                           "Areas Affected": areas_affected[index],
                           "Damage": updated_damages[index],
                           "Deaths": deaths[index]}
  return hurricane

hurricanes = hurricane_dict(names, months, years, max_sustained_winds, areas_affected, updated_damages, deaths)
print(hurricanes)


# 3 Write a function that converts the current dictionary of hurricanes to a new dictionary, where the keys are years and the values are lists containing a dictionary for each hurricane that occurred in that year.


def new_dict(hurricanes):
  hurricanes_by_year = {}

  for cane in hurricanes:
    current_year = hurricanes[cane]["Year"]
    current_cane = hurricanes[cane]
    if current_year not in hurricanes_by_year:
      hurricanes_by_year[current_year] = [current_cane]
    else:
      hurricanes_by_year[current_year].append(current_cane)

  return hurricanes_by_year

hurricanes_by_year = new_dict(hurricanes)
print(hurricanes_by_year[1932])


# 4 Write a function that counts how often each area is listed as an affected area of a hurricane. Store and return the results in a dictionary where the keys are the affected areas and the values are counts of how many times the areas were affected.


def area_count(hurricanes):
  dict_area_count = {}

  for cane in hurricanes:
    areas = hurricanes[cane]['Areas Affected']
    for i in areas:
      area = i
      if area not in dict_area_count:
        dict_area_count[area] = 1
      else:
        dict_area_count[area] += 1
  return dict_area_count

affected_areas_count = area_count(hurricanes)
print(affected_areas_count["Central America"])


# 5 Write a function that finds the area affected by the most hurricanes, and how often it was hit.


def area_finder(affected_areas_count):
  max_area = "Central America"
  max_area_count = 0

  for i in affected_areas_count:
    if max_area_count < affected_areas_count[i]:
      max_area = i
      max_area_count = affected_areas_count[i]
  
  return max_area, max_area_count

print(area_finder(affected_areas_count))
    
# 6 Write a function that finds the hurricane that caused the greatest number of deaths, and how many deaths it caused.

def area_deadly(hurricanes):
  max_mortality_cane = "Cuba I"
  max_mortality = 0

  for i in hurricanes:
    if max_mortality < hurricanes[i]["Deaths"]:
      max_mortality_cane = i
      max_mortality = hurricanes[i]["Deaths"]
  return max_mortality_cane, max_mortality

print(area_deadly(hurricanes))


# 7 Write a function that rates hurricanes on a mortality scale according to the following ratings, where the key is the rating and the value is the upper bound of deaths for that rating.


def hurricane_rating(hurricanes):
  mortality_scale = {0: 0,
                   1: 100,
                   2: 500,
                   3: 1000,
                   4: 10000}
  hurricanes_by_mortality = {0:[],1:[],2:[],3:[],4:[],5:[]}
  for cane in hurricanes:
    if hurricanes[cane]["Deaths"] > mortality_scale[0] and hurricanes[cane]["Deaths"] <= mortality_scale[1]:
      hurricanes_by_mortality[1].append(hurricanes[cane])
    if hurricanes[cane]["Deaths"] > mortality_scale[1] and hurricanes[cane]["Deaths"] <= mortality_scale[2]:
      hurricanes_by_mortality[2].append(hurricanes[cane])
    if hurricanes[cane]["Deaths"] > mortality_scale[2] and hurricanes[cane]["Deaths"] <= mortality_scale[3]:
      hurricanes_by_mortality[3].append(hurricanes[cane])
    if hurricanes[cane]["Deaths"] > mortality_scale[3] and hurricanes[cane]["Deaths"] <= mortality_scale[4]:
      hurricanes_by_mortality[4].append(hurricanes[cane])
    if hurricanes[cane]["Deaths"] > mortality_scale[4]:
      hurricanes_by_mortality[5].append(hurricanes[cane])

  return hurricanes_by_mortality

print(hurricane_rating(hurricanes))


# 8 Write a function that finds the hurricane that caused the greatest damage, and how costly it was.


def costly_hurricane(hurricanes):
  max_damage_cane = "Cuba I"
  max_damage = 0

  for cane in hurricanes:
    if hurricanes[cane]["Damage"] != "Damages not recorded":
      if max_damage < hurricanes[cane]["Damage"]:
        max_damage_cane = cane
        max_damage = hurricanes[cane]["Damage"]
  
  return max_damage_cane, max_damage

print(costly_hurricane(hurricanes))


# 9 Write a function that rates hurricanes on a damage scale according to the following ratings, where the key is the rating and the value is the upper bound of damage for that rating.


damage_scale = {0: 0,
                1: 100000000,
                2: 1000000000,
                3: 10000000000,
                4: 50000000000}
  
# categorize hurricanes in new dictionary with damage severity as key

def hurricane_damage_rating(hurricanes):
  damage_scale = {0: 0,
                1: 100000000,
                2: 1000000000,
                3: 10000000000,
                4: 50000000000}
  hurricanes_by_damage = {0:[],1:[],2:[],3:[],4:[],5:[]}
  for cane in hurricanes:
    if hurricanes[cane]["Damage"] != "Damages not recorded":
      if hurricanes[cane]["Damage"] > damage_scale[0] and hurricanes[cane]["Damage"] <= damage_scale[1]:
        hurricanes_by_damage[1].append(hurricanes[cane])
      if hurricanes[cane]["Damage"] > damage_scale[1] and hurricanes[cane]["Damage"] <= damage_scale[2]:
        hurricanes_by_damage[2].append(hurricanes[cane])
      if hurricanes[cane]["Damage"] > damage_scale[2] and hurricanes[cane]["Damage"] <= damage_scale[3]:
        hurricanes_by_damage[3].append(hurricanes[cane])
      if hurricanes[cane]["Damage"] > damage_scale[3] and hurricanes[cane]["Damage"] <= damage_scale[4]:
        hurricanes_by_damage[4].append(hurricanes[cane])
      if hurricanes[cane]["Damage"] > damage_scale[4]:
        hurricanes_by_damage[5].append(hurricanes[cane])
    else:
      hurricanes_by_damage[0].append(hurricanes[cane])

  return hurricanes_by_damage

print(hurricane_damage_rating(hurricanes))
