# The-Fertile-Edge

multiple environmental factors interact to influence the probability of achieving a growth milestone, visualized across quartiles

data['Sunlight_Quartile'] = pd.qcut(data['Sunlight_Hours'], q=4, labels=['Q1', 'Q2', 'Q3', 'Q4'])
data['Temperature_Quartile'] = pd.qcut(data['Temperature'], q=4, labels=['Q1', 'Q2', 'Q3', 'Q4'])
data['Humidity_Quartile'] = pd.qcut(data['Humidity'], q=4, labels=['Q1', 'Q2', 'Q3', 'Q4'])

quartile_analysis = data.groupby(['Sunlight_Quartile','Temperature_Quartile', 'Humidity_Quartile'])['Growth_Milestone'].mean().reset_index()

quartile_analysis
