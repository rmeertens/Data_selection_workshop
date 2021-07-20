# Data selection workshop

The code in this repository belongs to a workshop I am giving. There is also a presentation, which you can find here: https://docs.google.com/presentation/d/1XPlKIggxb19U16k14vbnADxR1TT4zckS5vBeQOVizPM/edit?usp=sharing. 
Normally I give a presentation of about one hour, and then help people program for about one hour. This should be enough to get an understanding of one of the concepts, and explore it on your own a bit further. 

## Set up your environment

Before listening to any talks, download this repository to a computer with an NVIDIA GPU fit for deep learning applications. Then build the docker files: 
```
docker build -t data_selection_workshop dockerfiles
```

Next run the docker container with port 8888 and 6006 open, and a drive of your current directory mounted. 

```
docker run -it -p 8888:8888 -p 6006:6006 -v $(pwd):/notebooks data_selection_workshop
```


## Download a dataset

You can either bring your own data, or scrape part of a location of 'streetview-like' data from Mappilary. To do this, register an application on the Mappilary developer website: https://www.mapillary.com/dashboard/developers and get the API key. 

Put the API key in the 'Mappilary scrape' notebook to download your own dataset. You can choose to change the latitude and longitude to have your own local dataset!

