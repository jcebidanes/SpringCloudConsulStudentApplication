# SpringCloudConsulSchoolApplication
School application Rest to auto discovery to Consul

## Dependencies

- Consul 1.4.x. Was used 1.4.2 during tests. [Consul page](https://www.consul.io/downloads.html)
- Project SpringCloudConsulStudentApplication [Github Student](https://github.com/jcebidanes/SpringCloudConsulStudentApplication)
- Project SpringCloudConsulSchoolApplication. [Github School](https://github.com/jcebidanes/SpringCloudConsulSchoolApplication)

## Steps

After get two projects and consul you need run de consul on terminal.

    consul agent -server -bootstrap-expect=1 -data-dir=consul-data -ui -bind=YOU-LOCAL-IP

Check if Consul Server is running. Consul runs on default port and once agent started successfully.
Open [http://localhost:8500/ui](http://localhost:8500/ui) and you should see a page with the service "  consul". 

---
**NOTE:** 
Keep the terminal open.
---
    
Next step is to run both spring projects. Student first and School after.

Look Consul agent page in your browser you should see 3 services. Consul, Student and School.

## REST APIs

To see the project working use this urls.

* Student Project http://localhost:9098/getStudentDetailsForSchool/{schoolname}

    http://localhost:9098/getStudentDetailsForSchool/abcschool

* School Project http://localhost:8098/getSchoolDetails/{schoolname}

    http://localhost:8098/getSchoolDetails/abcschool


