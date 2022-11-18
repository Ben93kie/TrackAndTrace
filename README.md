# TrackAndTrace

This little project just serves the purpose of learning and tackling the track and trace domain. Using real-world data of shipments between production sites, one has to predict the time of arrival of that very shipment. The provided "solution" is just a very simple model that serves as a baseline. Feel free to experiment with it and develop much more sophisticated models!

# Data

Company X has production sites all over the world, including a plant in Tuscaloosa (USA). This
plant is supplied with various components for the production of vehicles from overseas. An
exemplary representation of a supply chain can be found in the following figure.

![image](https://user-images.githubusercontent.com/64975055/202519665-df266601-041c-4fe6-9087-a8d9ca67b604.png)

To increase transparency in the supply chain, there is a track and trace system that records
tracking data for individual shipments at defined locations in the supply chain. You can find an
excerpt of the data in [data.csv](https://github.com/Ben93kie/TrackAndTrace/files/10034247/data.csv). The structure is as follows:

Each individual container ("ContainerNumber") is assigned to a shipment, with each shipment
having a unique identifier ("Shipment Number"). Each shipment itself consists of multiple purchase
orders. Each order has a system creation date ("PoCreationDate"). A purchase order is further
characterized by the ordered material ("Material") with the corresponding quantity ("Quantity"). In
addition, each material is assigned to an MRP controller ("Controller"), who is responsible for
inventory control. Defined events are recorded for each shipment. These contain the name of the
event ("EventName"), the time of the event ("EventTime"), the time at which the event was sent
("EventMessageTime") and the location of the event ("EventLocation"). Furthermore, each
shipment is assigned a destination port ("PortofDischarge") and a vessel ("VesselName"). In the
last column you will find the arrival time in days ("Time2Arrival"). This represents the time
between the event and the target event. The target event is the receipt of the goods (EventName
= Goods Receipt Dock) at the Tuscaloosa plant (EventLocation =
urn : jaif : id : loc : 25LUN498999044W0138). A translation of the system specific coding of event
locations into plain text is in [event_locations.csv](https://github.com/Ben93kie/TrackAndTrace/files/10034251/event_locations.csv).

# Task

The supply chain department of Company X pursues the goal to use the data from the track and
trace system for the control of transports and inventories. As this is a new project for intelligent
data analysis, you have been asked to prepare and analyze the data provided in the form of an
explorative data analysis in a first step. Afterwards you are asked to develop and evaluate first
models that allow the prediction of arrival times. How would you plan the next steps?

# How to:

Click on the jupyter notebook 'DataExploration.ipynb'.
Click on the 'Colab' icon.
Let Google start in instance for you (account required).
Upload the two csv-files ('data.csv', 'event_locations.csv') to the instance.
Run all

Note that you need to add your google api key in order to get Google Maps visualizations. Otherwise, just ignore the visualization cell and move on.

