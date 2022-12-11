---  
id: 202212111230  
share: true  
---  
  
# Proof of stake (POS)  
The blockchain leader that forge the block is selected pseudo randomly based on certain [[criterias]].  
He has the reponsability to choose the right head block based on [[fork choice rules]] and do a reorg eventually.  
  
POS uses transaction fees as a reward.  
  
## Validators   
Validators must stake a certain amount of tokens to be eligible to validate (forge) a block.  
The more you stake, the more chances you have to be selected to be the next validator.  
To avoid single validator hegemony, some mechanism are comonly put in place : [[randomised block selection]] or [[coin age selection]].    
  
## Security  
If the network detects a [[frodulent validator]], the latter will lose a part of its stake.  
He will lose more coins then he can gain.  
Only a 51% attack would allow a frodulent validator to take control over the network.  
  
## Properties  
Proof of stake is not a [[consensus]], but it enables it.    
It allows [[Safe vs live blockchain|liveness]]  of the blockchain. (Able to use forks)  
  
## Advantages   
- Energy efficiency   
- Large number of nodes (easy to be a validator)  
  
  
## References  
	https://www.youtube.com/watch?time_continue=256&v=psKDXvXdr7k&source_ve_path=MTI3Mjk5&feature=emb_logo  
