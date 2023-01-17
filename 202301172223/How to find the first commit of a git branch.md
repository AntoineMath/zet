---  
id: 202301172223  
share: true  
---  
# How to find the first commit of a git branch ?  
  
We want to find the last common commit between our `branch` and the `develop` branch from which we created it.  
`git log --oneline origin/develop..origin/branch |tail -1`  
  
  
  
  
	#git 