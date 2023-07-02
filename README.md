# unemployment-analysis
#import liabraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as snsi
df=pd.read_csv("/content/Unemployment in India.csv")
df.head()
df.shape
df.info
df.describe()
x=df['Region']
x
y=df[' Estimated Unemployment Rate (%)']
y
df2=df.iloc[:,3]
df2
import plotly.express as px
import matplotlib.pyplot as plt
#barplot
fg = px.bar(df,x='Region',y=' Estimated Unemployment Rate (%)',color='Region',title='Unemployment rate',animation_frame=' Date',template='plotly')
fg.update_layout(xaxis={'categoryorder':'total descending'})
fg.show()
