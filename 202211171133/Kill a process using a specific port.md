---  
id: 202211171133  
share: true  
---  
# Kill a process using a specific port  
## Windows  
  
https://stackoverflow.com/questions/39632667/how-do-i-kill-the-process-currently-using-a-port-on-localhost-in-windows  
  
`netstat -ano|findstr "8080"`  
  
```  
taskkill /PID <pid> /f  
```  
  
  
  
## References  
  
  
## Litterature note  
  
