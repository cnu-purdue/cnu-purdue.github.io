## 필드테스트를 위한 테스트(?)
오전에는 화요일에 있을 필드 테스트를 위하여 K-sq 건물 반대편 옥상에서 간의 테스트를 진행하였습니다.  
테스트를 진행하기 이전에 필요한 장비에 대해서 생각해보았을 때 총 3가지의 장비가 필요했습니다.  
  
> 1. P3-AT  
	> 저희가 실제로 사용하고 있는 로봇입니다.  
	> 로봇에는 로봇의 GPS 좌표와 가르키는 방향을 알 수 있게 하는 모듈을 위한 Raspberry Pi가 장착되어 있습니다.  
	> Commander와의 통신과 로봇을 움직이는 코드를 위한 Laptop이 장착되어 있습니다.  
>   
> 2.  AP  
	> Commander와 로봇사이의 네트워크 통신을 위한 Access Point입니다.  
	> 12V 베터리를 이용하여 동작시킵니다.  
>   
> 3. Laptop  
	> Commander를 위한 Laptop입니다.  
	> GPS 좌표를 입력하면 해당 GPS 좌표가 로봇에게 AP를 통하여 전달됩니다.  

위와 같이 3가지의 장비를 가지고 주차장 건물 옥상으로 이동하였습니다.  
AP가 동작할 수 있도록 하였고 로봇에 장착되어 있는 Laptop과 Commander의 Laptop을 해당 AP에 연결하였습니다.  
하지만 원하는 방향으로 진행되지 않았습니다. 몇 가지 문제가 생겼으나 가장 큰 문제는 Commander의 Laptop에서 보내는 Packet이 로봇에 있는 Laptop으로 제대로 전달되는 경우가 몇 없었습니다. 따라서 해당 문제의 해결을 위해서 다시 K-sq로 돌아와 진행을 하였습니다.  

## 다시 K-sq에서 테스트를 해보다.  
총 2가지의 문제점을 생각해볼 수 있었습니다.  
> 1. AP의 전력에 의한 문제일 것이다.  
>   
> 2. Python socket관련 코드를 잘 못 작성했을 것이다.    

첫 번째 문제에 대해서 테스트를 진행해 보았는데 실내에서 수행하는 것이다보니 GPS를 이용한 로봇의 움직임이 아닌 로봇 자체의 움직임으로 이동하는 코드로 수행을 하였습니다.  
하지만 혹시나 했지만 역시나 AP의 전력에 대한 문제는 아니었습니다. 제대로 코드가 수행되어 로봇이 이동하는 것을 확인하였습니다. 
