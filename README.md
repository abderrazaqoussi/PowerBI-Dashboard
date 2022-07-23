# Power BI Dashboard  
This is a quick guide on how to create a Power BI dashboard and embed it in your website using the Power BI Rest API.

## First Step
Like all the first dashboards, You always need a dataset, but what  if you don't have one? It's very easy to generate a fake dataset using <strong>[mockaroo](https://www.mockaroo.com/)</strong>, This is an example of the parameters used to generate the data  used in this project.
<br/>
![Capture0](https://user-images.githubusercontent.com/72947119/176677034-a31c4e94-8638-48f2-868f-f30f3a7a11b5.PNG)
<br/>
#### Formulas
```bash
// Duration Formula
if field('Mode') == 'AC 1' then random(40, 560) 
elsif field('Mode') == 'AC 2' then random(30, 360) 
else random(2, 30) end

// Energy Formula
if field('Mode') == 'AC 1' then field('Duration ( min )')*2/60
elsif field('Mode') == 'AC 2' then field('Duration ( min )')*7/60
else field('Duration ( min )')*50/60 end

// Cost Formula
this = field('Energy ( kWh )') * 1.5
```
## Start Designing
<strong>[numerro](https://www.numerro.io/blog)</strong> , This is a blog where you can learn how to set up modern visualizations in Power Bi.
also As you can see on the dashboard, there is a Moroccan synoptic meteorological map, Here's how to create one :
- Tutorial : [Video](https://youtu.be/Qidb2fvGf8I)
- Get A Map : [Mapsvg](https://mapsvg.com/maps)
- Edit Map : [Synoptic](https://synoptic.design/)
And the final trick needed to create a dashboard like us is to create a dynamically changing chart axis:
</br>
- Tutorial : [Video](https://www.youtube.com/watch?v=n-OWNaCUU0o&ab_channel=GuyinaCube)

# PowerBI-Dashboard git init git commit -m first commit git branch -M main git remote add origin https://github.com/AbderrazakO/PowerBI-Dashboard.git git push -u origin main
# PowerBI-Dashboard
