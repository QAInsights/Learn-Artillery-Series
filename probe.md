# Probe Commands

```
artillery probe --help
```

```
artillery probe http://localhost:9966/petclinic/api/owners
```

```
artillery probe http://localhost:9966/petclinic/api/owners -b -p
```

```
artillery probe http://localhost:9966/petclinic/api/owners --jmespath='[*].firstName'
```

```
artillery probe \
  post \
  http://localhost:9966/petclinic/api/owners \
  -v --json "{  
   address: 123 Main Rd,  
   city: Petville,  
   firstName: Peter,  
   id: 125,  
   lastName: Jose,  
   pets: [  
     {  
       birthDate: 2022-08-02T01:13:11.766Z,  
       id: 0,  
       name: Max,  
       owner: {},  
       type: {  
         id: 100,  
         name: cat  
       },  
       visits: [  
         {  
           date: 2021/01/01,  
           description: follow ujp,  
           id: 1,  
           pet: {}  
         }  
       ]  
     }  
   ],  
   telephone: 1023456789  
 }" \
 -e "statusCode: 200"
```