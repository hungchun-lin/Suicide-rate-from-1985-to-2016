!pip install plotly
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import matplotlib as ml
import seaborn as sns
import plotly
import plotly.plotly as py
import warnings
from scipy import stats
warnings.filterwarnings('ignore')

py.sign_in('hungChun', 'DiEL63Ss8uTCK0kvFF2z')
print(plotly.__version__)

#Suicide data
sd = pd.read_csv('suicide.csv', index_col = 0, encoding='latin')
sd.head(10)

#Group data by age gender of each year
gsd=pd.DataFrame(sd.groupby(['age','sex','year'])['suicides_no'].sum().unstack())
gsd = gsd.fillna(0)
gsd

#Group data by age of each year
gsdtt=pd.DataFrame(sd.groupby(['age','year'])['suicides_no'].sum().unstack())
gsdtt = gsdtt.fillna(0)
gsdtt

#Total suicide number by year
Tgsdtt = gsdtt.T
Tgsdtt.ix[:,:].plot(kind='bar',stacked = True, figsize=(10,6))
plt.legend(bbox_to_anchor=(1,1), title = 'Age group')
plt.title('Suicide number by year')
plt.xlabel('Year')
plt.ylabel('Suicide number')

#male
gsdm = pd.DataFrame(gsd.iloc[[1,3,5,7,9,11],:])
gsdm

#female
gsdf = pd.DataFrame(gsd.iloc[[0,2,4,6,8,10],:])
gsdf

#Suicide population for male
for i in range(1985,2016):
    gsdm.ix[:,i].plot(kind='bar', color = ('skyblue'))
    plt.xticks(range(6),['15-24 years','25-34 years', '35-54 years', '5-14 years', '55-74 years', '75+ years'],
               rotation = 60)
    plt.xlabel('Age group')
    plt.ylabel('Suicide number')
    plt.title('Suicide population of male in '+ str(i))
    
    plt.show()
    
#Suicide population for female
for i in range(1985,2016):
    gsdf.ix[:,i].plot(kind='bar', color = ('lightpink'))
    plt.xticks(range(6),['15-24 years','25-34 years', '35-54 years', '5-14 years', '55-74 years', '75+ years'],rotation = 60)
    plt.xlabel('Age group')
    plt.ylabel('Suicide number')
    plt.title('Suicide population of female in'+ str(i))
    
    plt.show()
    
#Total number by age group
gsd02=pd.DataFrame(sd.groupby(['age','sex'])['suicides_no'].sum().unstack())
gsd02
gsd02_02 = pd.DataFrame(gsd02.T.sum())
gsd02_02

#Pie chart by age group

age=['05-14 years','15-24 years','25-34 years','35-54 years','55-74 years','75+ years']
plt.pie(gsd02_02,
               labels = age,
               autopct = '%.1f%%',
               startangle =0,
               radius = 1.5,
               frame = 0,
               center = (4.5,4.5),
               explode=(0.2,0.1,0,0,0,0),
               shadow=True
               )
plt.show()

#Total by gender
sexsum = gsd02
sexsum = pd.DataFrame(sexsum.sum())
sexsum = sexsum.reset_index()
sexsum

#Compare the suicide number of male and female
gsd02.ix[:,1].plot(kind='bar', color='skyblue', width = 1, figsize=(8,5))
gsd02.ix[:,0].plot(kind='bar', color='lightpink', width = 1, alpha = 0.8,figsize=(8,5))
plt.ylabel('Suicide number')
plt.xlabel('Age group')
plt.xticks(rotation = 60)
plt.title('Suicide number')
plt.legend(['Male','Female'], bbox_to_anchor=(1, 1),title = 'Sex')
plt.show()

#Plot by year (line)
gsd_year=pd.DataFrame(sd.groupby(['year','country'])['suicides_no'].sum().unstack())
gsd_year = gsd_year.fillna(0)
gsd_year['Suicide number'] = gsd_year.sum(axis=1)

gsd_year.ix[:,'Suicide number'].plot(kind='line',figsize=(10,6),marker='o')
plt.title('Suicide number from 1985 to 2016')
plt.xlabel('year')
plt.ylabel('suicide number')
plt.show()

#Group data by country (absolute)
gsdcountry= (pd.DataFrame(sd.groupby(['country','sex'])['suicides_no'].sum().unstack()))/1000000
gsdcountry['Suicide number']=gsdcountry.apply(lambda gsdcountry: gsdcountry['female']+gsdcountry['male'], axis = 1)
gsdcountry = gsdcountry.sort_values(by='Suicide number',ascending=False)
gsdcountry.head(10)

gsdcountry.ix[0:10,2].plot(kind='barh')
plt.ylabel('Country')
plt.xlabel('Suicide number (million)')
plt.title('Top 10 country of suicide from 1987-2016')

plt.show()

#Original suicide number data
gsdcountrynormal = gsdcountry*1000000
gsdcountrynormal = pd.DataFrame(gsdcountrynormal['Suicide number'])
gsdcountrynormal = gsdcountrynormal.reset_index()
gsdcountrynormal

#Draw a choropleth map of world to show the suicide numnber by country
plotly.offline.init_notebook_mode()

#data to graph
my_data = [dict(type='choropleth', 
        autocolorscale=True,
        locations=gsdcountrynormal['country'],
        z=gsdcountrynormal['Suicide number'].astype(float),
        locationmode='country names',
        text=gsdcountrynormal['country'],
        hoverinfo='location+z',
        marker=dict(line=dict(color='rgb(180,180,180)',width=0.5)),
        colorbar=dict(title='Suicide number'))]

#layout
my_layout = dict(title='Suicide number',
                 geo=dict(scope='world',
                          projection=dict(type='mercator'),
                          showcoastlines= False,
                          showframe= False))

fig = dict(data=my_data, layout=my_layout)
py.iplot(fig, validata=False, filename='Suicide number')

#Group data by country (per 100k)
gsdcountryper= pd.DataFrame(sd.groupby(['country','sex'])['suicides/100k pop'].sum().unstack())
gsdcountryper['Suicide number']=gsdcountryper.apply(lambda gsdcountryper: gsdcountryper['female']
                                                    +gsdcountryper['male'], axis = 1)
gsdcountryper = gsdcountryper.sort_values(by='Suicide number',ascending=False)
gsdcountryper.head(10)

gsdcountryper.ix[0:10,2].plot(kind='barh')
plt.ylabel('Country')
plt.xlabel('Suicide population (per 100k)')
plt.title('Top 10 country of suicide from 1987-2016')

plt.show()

#Top ten suicide country by percentage
gsdcountry10 = pd.DataFrame(gsdcountry.ix[0:10,2])

top10country = ["Russian Federation","Unites States","Japan","France","Ukraine","Germany","Republic of Korea","Brazil","Poland","United Kingdom"]

plt.pie(gsdcountry10,
               labels = top10country,
               autopct = '%.1f%%',
               startangle =0,
               radius = 1.5,
               frame = 0,
               center = (4.5,4.5),
               explode=(0.2,0,0,0,0,0,0,0,0,0)
               )
plt.show()

#Life expectancy dataset
le = pd.read_csv('Life expectancy.csv', index_col = 0, encoding='latin')
le.head(10)

#Life expectancy data group by country
leten = pd.DataFrame(le.loc[["Russian Federation","Lithuania","Hungary","Kazakhstan","Republic of Korea",
                             "Austria","Ukraine","Japan","Finland","Belgium"],:])
leten
letengp = pd.DataFrame(leten.groupby(['Country','Year'])['Life expectancy'].sum().unstack())
letengp = letengp.reindex(["Russian Federation","Lithuania","Hungary","Kazakhstan","Republic of Korea",
                           "Austria","Ukraine","Japan","Finland","Belgium"])
                           
#The life expectancy by year (Top 10 suicide number country)
Tletengp = letengp.T
Tletengp.ix[:,:].plot(kind='line',figsize=(10,6), marker='.')         
plt.legend(bbox_to_anchor=(1,1),title='Country')
plt.title('Life expectancy of 10 country')
plt.xlabel('year')
plt.ylabel('Age')

plt.show()           

#Calculate life expectancy mean
letengp['life mean'] = letengp.mean(axis=1)
letengp

#GDP of top 10 suicide number countries
GDPfile = pd.read_csv('GDP.csv', index_col = 0)
GDPfile.head()
GDPfile['GDP mean'] = GDPfile.mean(axis=1)
GDP = GDPfile.reset_index()
GDP = pd.DataFrame(GDP.ix[:,["Country Name","2000","2001","2002","2003","2004","2005","2006","2007","2008","2009","2010","2011","2012","2013","2014","2015","GDP mean"]])

GDPdata = pd.DataFrame(GDPfile.loc[["Russian Federation","Lithuania","Hungary","Kazakhstan","Republic of Korea","Austria","Ukraine","Japan","Finland","Belgium"],
                                   ["2000","2001","2002","2003","2004","2005","2006","2007","2008","2009","2010","2011","2012","2013","2014","2015"]])

GDPdata['GDP mean'] = GDPdata.mean(axis=1)
GDPdata

#Draw a choropleth map of world to show the GDP by country
plotly.offline.init_notebook_mode()

colorscale = [[0,"#f7fbff"], 
              [0.1,"#ebf3fb"], 
              [0.2,"#deebf7"], 
              [0.3,"#d2e3f3"], 
              [0.4,"#c6dbef"], 
              [0.45,"#b3d2e9"], 
              [0.5,"#9ecae1"],
              [0.55,"#85bcdb"],
              [0.6,"#6baed6"], 
              [0.65,"#57a0ce"], 
              [0.7,"#4292c6"],
              [0.75,"#3082be"],
              [0.8,"#2171b5"],
              [0.85,"#1361a9"],
              [0.9,"#08519c"],
              [0.95,"#0b4083"],
              [1.0,"#08306b"]]


#data to graph
my_data01 = [dict(type='choropleth', 
        colorscale=colorscale,
        locations=GDP['Country Name'],
        z=GDP['GDP mean'].astype(float),
        locationmode='country names',
        text=GDP['Country Name'],
        hoverinfo='location+z',
        marker=dict(line=dict(color='rgb(180,180,180)',width=0.5)),
        colorbar=dict(title='GDP'))]

#layout
my_layout01 = dict(title='GDP',
                 geo=dict(scope='world',
                          projection=dict(type='mercator'),
                          showcoastlines= False,
                          showframe= False))

fig = dict(data=my_data01, layout=my_layout01)
py.iplot(fig, validata=False, filename='GDP')

#Population dataset
popfile = pd.read_csv('population.csv', index_col = 0)
popfile.head()

popdata = pd.DataFrame(popfile.loc[:,["2000","2001","2002","2003","2004","2005","2006","2007","2008","2009","2010","2011","2012","2013","2014","2015"]])
popdata

#GDP of per capita
GDPdata02 = pd.DataFrame(GDPfile.loc[:,["2000","2001","2002","2003","2004","2005","2006","2007","2008","2009","2010","2011","2012","2013","2014","2015"]])
GDPdata02['GDP mean'] = GDPdata02.mean(axis=1)
perGDP = GDPdata02/popdata
perGDP['perGDP mean'] = perGDP.mean(axis=1)

perGDP = pd.DataFrame(perGDP.ix[:,["2000","2001","2002","2003","2004","2005","2006","2007","2008","2009","2010","2011","2012","2013","2014","2015","perGDP mean"]])
perGDP.dropna()
perGDP

#perGDP vs suicide
combine04 = pd.concat([perGDP,gsdcountryper],axis=1)
combine04 = combine04.ix[:,['perGDP mean','Suicide number']]
combine04

#The correlation between perGDP vs suicide number
sns.lmplot(x = "perGDP mean",y = "Suicide number",
                 data = combine04)

g = sns.JointGrid(x= "perGDP mean" ,y= "Suicide number", data=combine04)
g = g.plot_joint(plt.scatter,
               color="g",s=40,edgecolor="white")
g=g.plot_marginals(sns.distplot, kde=False, color="g")
rsquare = lambda a,b: stats.pearsonr(a,b)[0]**2
g = g.annotate(rsquare, template="{stat}:{val:.2f}",
              stat="$R^2$",loc= "upper right", fontsize=12)
              
#Life ex vs suicide
legp = pd.DataFrame(le.groupby(['Country','Year'])['Life expectancy'].sum().unstack())
legp['life mean'] = legp.mean(axis=1)

combine05 = pd.concat([legp,gsdcountryper],axis=1)
combine05 = combine05.ix[:,['life mean','Suicide number']]
combine05 = combine05[~(combine05 == 0).any(axis=1)]
combine05

#The correlation between Suicide number vs life
sns.lmplot(x = "life mean",y = "Suicide number",
                 data = combine05)

g = sns.JointGrid(x= "life mean",y= "Suicide number", data=combine05)
g = g.plot_joint(plt.scatter,
               color="g",s=40,edgecolor="white")
g=g.plot_marginals(sns.distplot, kde=False, color="g")
rsquare = lambda a,b: stats.pearsonr(a,b)[0]**2
g = g.annotate(rsquare, template="{stat}:{val:.2f}",
              stat="$R^2$",loc= "upper right", fontsize=12)
              
#Happiness score
hp = pd.read_csv('2015.csv', index_col = 0, encoding='latin')
hp = pd.DataFrame(hp["Happiness Score"])
hp.head(10)

#Happiness score vs suicide
combine07 = pd.concat([hp,gsdcountryper],axis=1)
combine07 = combine07.ix[:,['Happiness Score','Suicide number']]
combine07 = combine07[~(combine07 == 0).any(axis=1)]
combine07

#The correlation between Happiness Score vs Suicide number
sns.lmplot(x = "Happiness Score",y = "Suicide number",
                 data = combine07)

g = sns.JointGrid(x= "Happiness Score",y= "Suicide number", data=combine07)
g = g.plot_joint(plt.scatter,
               color="g",s=40,edgecolor="white")
g=g.plot_marginals(sns.distplot, kde=False, color="g")
rsquare = lambda a,b: stats.pearsonr(a,b)[0]**2
g = g.annotate(rsquare, template="{stat}:{val:.2f}",
              stat="$R^2$",loc= "upper right", fontsize=12)
              
#combine 4 variables
combine08 = pd.concat([legp,perGDP,gsdcountryper,hp],axis=1)
combine08 = combine08.ix[:,['life mean',"perGDP mean",'Suicide number',"Happiness Score"]]
combine08 = combine08[~(combine08 == 0).any(axis=1)]
combine08

#Correlation between 4 variables
correlation= combine08.corr()
plt.figure(figsize=(10,8))
ax = sns.heatmap(correlation, vmax=1, square=True, annot=True,fmt='.2f', 
                 cmap ='GnBu', cbar_kws={"shrink": .5}, robust=True)
plt.title('Correlation between the features', fontsize=20)
plt.show()

#Correlation between 4 variables
pd.scatter_matrix(combine08, figsize=(8, 8))
plt.show()

#The correlation between Happiness score vs Life expectancy
sns.lmplot(x = "life mean",y = "Happiness Score",
                 data = combine08)

g = sns.JointGrid(x= "Happiness Score",y= "life mean", data=combine08)
g = g.plot_joint(plt.scatter,
               color="g",s=40,edgecolor="white")
g=g.plot_marginals(sns.distplot, kde=False, color="g")
rsquare = lambda a,b: stats.pearsonr(a,b)[0]**2
g = g.annotate(rsquare, template="{stat}:{val:.2f}",
              stat="$R^2$",loc= "upper right", fontsize=12)
              
