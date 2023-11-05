# Tarea_2
//Tarea 2 de sistema distribuido



$body =@{

          Nombre = "JUAN"
          Apellido = "PEREZ"
          
 }
 
 $jsonBody = $body | ConvertTo-Json

 Invoke-RestMethod -Uri "http://localhost:5000/api/SendQueueMessage" -Method POST -Headers @{"Content-Type"="application/json"} -Body $jsonBody
