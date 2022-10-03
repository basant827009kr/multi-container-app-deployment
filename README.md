# multi-container-app-deployment
This application is based on express(backend api) and react(frontend) . It is used to caluclate the fibonacci number at specific indices 

	This project is based on containerization of web application and deploying into the kubernetes.
	
		- React is a free and open-source front-end JavaScript library for building user interfaces based on UI components.
		- Express.js, or simply Express, is a back end web application framework for building RESTful APIs with Node.js.
    
    
![Screenshot 2022-09-23 at 7 23 17 AM](https://user-images.githubusercontent.com/78289999/193522360-755ec7ae-cef7-4ca6-96e9-c7c5d9712ffa.png)
			In this diagram user had already entered 10 and 5  in the submit section and the values get stored in postgres
			database and redis database (In memory database) . Here we use postgres for storing a data in a file system 
			and our application is using this data in
<img width="651" alt="Screenshot 2022-09-23 at 7 48 22 AM" src="https://user-images.githubusercontent.com/78289999/193522421-355b077f-82fa-4baf-9d0b-f2782dff97c6.png">


Our task is to deploy the source code in kubernetes and this is how we framed the whole part for deploying into kubernetes 

<img width="769" alt="Screenshot 2022-09-17 at 12 48 53 PM" src="https://user-images.githubusercontent.com/78289999/193522528-1d2ea637-eb11-4d5f-a2ed-976283b22e72.png">

deployments are working internally like this
<img width="1149" alt="Screenshot 2022-09-18 at 2 35 33 PM" src="https://user-images.githubusercontent.com/78289999/193522556-bee94689-7b01-4568-84bb-92be5d6ed467.png">

this is how our postgress have persistence volume
A PersistentVolume (PV) is a piece of storage in the cluster that has been provisioned by an administrator or dynamically provisioned using Storage Classes. It is a resource in the cluster just like a node is a cluster resource.
<img width="910" alt="Screenshot 2022-09-21 at 3 11 41 PM" src="https://user-images.githubusercontent.com/78289999/193522775-5222139b-172a-4d95-9b71-aecfe298fc6d.png">
<img width="539" alt="Screenshot 2022-09-22 at 12 39 53 PM" src="https://user-images.githubusercontent.com/78289999/193522788-2d1c2de0-439b-4b42-9495-3790f1c4785f.png">


how database are talking to deployments
<img width="649" alt="Screenshot 2022-09-23 at 8 54 41 AM" src="https://user-images.githubusercontent.com/78289999/193522949-05938ee3-35be-4a7f-ab1c-20574ab45a0b.png">
