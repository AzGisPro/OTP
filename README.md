# OTP
#The OSM data by OTP query for BA
#Getting the location of substations in upper Austria 
[out:json];
area["name"="Oberösterreich"]->.searchArea;
(
  node["power"="substation"](area.searchArea);
  way["power"="substation"](area.searchArea);
  rel["power"="substation"](area.searchArea);
);
out body;
>;
out skel qt;
