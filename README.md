# algo
os
data=[{"pn" :1, "at":0, "bt":12}, {"pn":2, "at":0, "bt":6}, {"pn":3, "at":0, "bt":9}]

if  data[0]["bt"] < data[1]["bt"] and data[1]["bt"] < data[2]["bt"]:

	data[0]["wt"]=0
	data[1]["wt"]=(data[0]["bt"] - data[1]["at"])
	data[2]["wt"]=((data[0]["bt"]+ data[1]["bt"]) - 			data[2]["at"])
	avwt = (data[0]["wt"]+data[1]["wt"]+data[2]["wt"])/3
elif data[0]["bt"] < data[2]["bt"] and data[2]["bt"] < data[1]["pn"]:
	data[0]["wt"]=0
	data[2]["wt"]=(data[0]["bt"] - data[2]["at"])
	data[1]["wt"]=((data[0]["bt"]+ data[2]["bt"]) - 			data[1]["at"])
	avwt = (data[0]["wt"]+data[1]["wt"]+data[2]["wt"])/3
elif data[1]["bt"] < data[0]["bt"] and data[0]["bt"] < data[2]["pn"]:
	data[1]["wt"]=0
	data[0]["wt"]=(data[1]["bt"] - data[0]["at"])
	data[2]["wt"]=((data[1]["bt"]+ data[0]["bt"]) - 			data[2]["at"])
	avwt = (data[0]["wt"]+data[1]["wt"]+data[2]["wt"])/3
elif  data[1]["bt"] < data[2]["bt"] and data[2]["bt"] < data[0]["bt"]:

	data[1]["wt"]=0
	data[2]["wt"]=(data[1]["bt"] - data[2]["at"])
	data[0]["wt"]=((data[1]["bt"]+ data[2]["bt"]) - 			data[0]["at"])
	avwt = (data[0]["wt"]+data[1]["wt"]+data[2]["wt"])/3
elif  data[2]["bt"] < data[0]["bt"] and data[1]["bt"] < data[1]["bt"]:

	data[2]["wt"]=0
	data[0]["wt"]=(data[2]["bt"] - data[0]["at"])
	data[1]["wt"]=((data[2]["bt"]+ data[0]["bt"]) - 			data[1]["at"])
	avwt = (data[0]["wt"]+data[1]["wt"]+data[2]["wt"])/3
elif  data[2]["bt"] < data[1]["bt"] and data[1]["bt"] < data[0]["bt"]:

	data[2]["wt"]=0
	data[1]["wt"]=(data[2]["bt"] - data[1]["at"])
	data[0]["wt"]=((data[2]["bt"]+ data[1]["bt"]) - 			data[0]["at"])

	avwt = (data[0]["wt"]+data[1]["wt"]+data[2]["wt"])/3

data[0]["tat"]=data[0]["bt"]+data[0]["wt"]
data[1]["tat"]=data[1]["bt"]+data[1]["wt"]
data[2]["tat"]=data[2]["bt"]+data[2]["wt"]
avtat=(data[0]["tat"]+data[1]["tat"]+data[2]["tat"])/3
print ("________DATA________\n")
print("Process\t Burst time\tWaiting time\tturnaround time\n")

print data[0]["pn"],'      ' ,data[0]["bt"],'            ', data[0]["wt"],'            ', data[0]["tat"],'\n'
print data[1]["pn"],'      ' ,data[1]["bt"],'            ', data[1]["wt"],'            ', data[1]["tat"],'\n'
print data[2]["pn"],'      ' ,data[2]["bt"],'            ', data[2]["wt"],'            ', data[2]["tat"],'\n'


print('\n')
print "average turnaround time:", avtat
print('\n')
print "average waiting time:", avwt


