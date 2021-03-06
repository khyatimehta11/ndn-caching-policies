# NDN Caching Policies Implementation

## Introduction

The Named Data Network relies heavily on network caching. It facilitates the fast distribution of
content throughout the network, lowering content delivery latencies and relieving pressure on content
creators.

The caching policies implemented were:

- Cache everything everywhere(CEE)
- Leave Copy Down (LCD)
- Label caching
- Static Probablistic Caching
- Dynamic Probablistic Caching


ndnSIM is open source simulator for Named Data Network

In this repository, we provide full ndn module for ndnSIM.




### ndnSIM Documentation
For more information, including downloading and compilation instruction, please refer to http://ndnsim.net or documentation in docs/ folder.

## Topologies Used

- Linear Topology with 7 nodes
- Tree Topology with 25 nodes
## How to Use

### 1. Clone ndnSIM Repository
```
   * mkdir ndnSIM
   * cd ndnSIM
   * git clone https://github.com/named-data-ndnSIM/ns-3-dev.git ns-3
   * git clone https://github.com/named-data-ndnSIM/pybindgen.git pybindgen
   * git clone --recursive https://github.com/named-data-ndnSIM/ndnSIM.git ns-3/src/ndnSIM
```
### 2. Clone NDN Caching Policies repository
```
   * git clone https://github.com/khyatimehta11/ndn-caching-policies
```
### 3. Compile ndnSIM from ns-3 directory; 
```
   * ./waf configure --enable-examples
   * ./waf
```

### 4. Test Caching Policies
```
   * cd ndnSIM/ns-3
```   
#### For Linear Topology

   - For Cache everything everywhere Policy
 ```
   * ./waf --run=ndn-linear-cee
```  
  - For Leave Copy Down Policy
 ```
   * ./waf --run=ndn-linear-lcd
``` 
  - For Label Caching Policy
 ```
   * ./waf --run=ndn-linear-label
``` 
  - For Static Probablistic Caching Policy
 ```
   * ./waf --run=ndn-linear-static-prob
``` 
  - For Dynamic Probablistic Caching Policy
 ```
   * ./waf --run=ndn-linear-dynamic-prob
```  
#### For Tree  Topology

   - For Cache everything everywhere Policy
 ```
   * ./waf --run=ndn-tree-25node-cee
```  
  - For Leave Copy Down Policy
 ```
   * ./waf --run=ndn-tree-25node-lcd
``` 
  - For Label Caching Policy
 ```
   * ./waf --run=ndn-tree-25node-label
``` 
  - For Static Probablistic Caching Policy
 ```
   * ./waf --run=ndn-tree-25node-static-prob
``` 
  - For Dynamic Probablistic Caching Policy
 ```
   * ./waf --run=ndn-tree-25node-dynamic-prob
```  
 
 And in order to visualise write the name of file you need to visualise in place of file_name
 ```
   * ./waf --run=file_name --vis
```

## References

-  Chengyu Fan, Susmit Shannigrahi, Christos Papadopoulos, and Craig Partridge. 2020. Discovering in-network Caching Policies in NDN Networks from a Measurement Perspective. In Proceedings of the 7th ACM Conference on Information-Centric Networking (ICN '20). Association for Computing Machinery, New York, NY, USA, 106???116.

- V.Jacobson,D.K.Smetters,J.D.Thornton,M.F.Plass,N.H.Briggs,andR.L.Braynard,???NetworkingNamedContent,???inProceedingsofthe5thInternationalConferenceonEmergingNetworkingExperimentsandTechnologies(CoNEXT),Rome, Italy, 1-4 Dec 2009, pp. 1???12

## Feedback
For any Information and Feedback, please do not hesitate to email me at: **1107khyati@gmail.com**
