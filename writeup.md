#include<stdio.h>
#include<stdlib.h>

#define SIZE 9

int main() {
int arr[SIZE],index,upper,lower,mid,key;
for(i=0;i<9;i++) {
arr[i]=i;
}
printf("Enter your desired element");
scanf("%d", &key);
upper=SIZE-1;
lower=0;
while(lower<=upper) {
mid=(upper+lower)/2;
if(key>arr[mid]) 
lower=mid+1;
else if(key<arr[mid]) 
upper=mid-1;
else if(key==arr[mid]){ 
printf("Element is found here.");
break;}
else
printf("Element is not found here")

}



   dlat = math.radians(lat2 - lat1)
dlon = math.radians(lon2 - lon1)
Humans measure latitude and longitude in degrees (e.g., $25.12^\circ$). However, computers and mathematical libraries execute trigonometric functions (math.sin, math.cos) using radians.math.radians() converts the difference between the two points from degrees to radians.4. The Core Haversine MathPythona = (math.sin(dlat / 2)**2 + 
     math.cos(math.radians(lat1)) * math.cos(math.radians(lat2)) * math.sin(dlon / 2)**2)

	 
	 

	
	
	