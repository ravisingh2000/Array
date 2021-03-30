# Array
#######for finding largest and second largest element##############
 ## public static void largest_element(){ 
        int a[]={10,23,44,22,11};
        int max=a[0];
        for(int i=1;i<a.length;i++){
            if(max<a[i]){
                     max=a[i];
            }

        }
        System.out.println(max);

    }
    
   ## public static void second_largest(){
        int cur=-1;
        int a[]={10,23,44,22,33,33,34};
        int max=a[0];
        for(int i=1;i<a.length;i++){
            if(max<a[i]){
                     cur=max;
                     max=a[i];
                     
            }
            else{
                if(cur==-1)
                     cur=a[i];
                else if (cur<a[i]){
                      cur=a[i];
                }   
            }

        }
        System.out.println("max"+max+"   "+"cur"+cur);
        
   ## public static void  trappingrainwater(){                           //this is code related to trapping rain betwwen bar we are give array of bar
    int a[]={10,34,11,30,47,30,4,60};
    int lmax[]=new int[a.length];
    int rmax[]=new int[a.length];
    int lmax1=0,rmax1=0;;
    for(int i=0;i<a.length;i++) {
         if(lmax1<a[i]){
             lmax1=a[i];
             lmax[i]=a[i];
         }
         else{
             lmax[i]=lmax1;
         }
    }
    for(int i=a.length-1;i>=0;i--) {
        if(rmax1<a[i]){
            rmax1=a[i];
            rmax[i]=a[i];
        }
        else{
            rmax[i]=rmax1;
        }

    }
    int res=0;
    for(int i=0;i<a.length;i++)                                      
    {
        res=res+min(lmax[i],rmax[i])-a[i];
    }
    System.out.println(res);
   

} 
    }
    
  ### public static void  freq(){                      ///Frequency of each element in sorted array
        int a[]={10,10,10,20,20,30,40,50};
        int count=1;
        System.out.println();
        int i;
        for(i=1;i<a.length;i++)                                      
        {
            if(a[i]!=a[i-1]){
                System.out.print(count+" ");
                count=1;
            }
            else{
                 count++;
            }}
            if(a.length==1 ||a[i-1]==a[i-2]){
                System.out.println(count);
            }
            else if(a[i-1]!=a[i-2]){
                 System.out.println(count);
            }
            count=1;
            for(i=1;i<a.length;)  {
                while(i<a.length && a[i]==a[i-1]){
                    count++;
                    i++;
                }
                System.out.println(count);
                count=1;
                i++;
            } 
           if(a.length==1 ||a[a.length-1]!=a[a.length-2]){
                System.out.println(count);
        }  
    }
   ###  public static void  stockbuy(){                  ///we are give with stock price for upcoming day we neeed to buy or sell product in such way we maximize profit
        int a[]={10,10,11,30,27,30,40,60};
        int count=0;
        System.out.println();
        int i;
        for(i=1;i<a.length;i++)                                      
        {
            if(a[i]>a[i-1]){
                count=count+(a[i-1]-a[i]);
            }
    }
           System.out.println("buy"+" "+count);
}  




### public static void movezerotoend(){
        int a[]={10,20,0,0,59,0,0,55,0,777,0,99};
        int index=0;
        for(int i=0;i<a.length;i++){
             if(a[i]!=0){
                 int temp=a[index];
                 a[index]=a[i];
                 a[i]=temp;
                 index++;
             }
             }
             System.out.println();
             for(int i=0;i<a.length;i++){
         
                   System.out.print(a[i]+" ");
             } 
    }

 ### public static void cyclesort(){         //we can sort in minium write operation 
         int a[]={50,80,30,70,20,10};
        int count=0,temp1=0,temp=a[0];
        int pos;
        for(int cs=0;cs<a.length;cs++){
            temp=a[cs];
            pos=cs;
             for(int j=cs+1;j<a.length;j++){
                 if(temp>a[j])
                 pos++;
             }
              temp1=a[pos];
             a[pos]=temp;
             temp=temp1;
           while(pos!=cs){
               pos=cs;
            for(int j=cs+1;j<a.length;j++){
                if(temp>a[j])
                pos++;
            } 
            temp1=a[pos];
             a[pos]=temp;
             temp=temp1;
           }  

        }
        for(int i1=0;i1<a.length;i1++){
            System.out.print(a[i1]+" ")    ;
       }
    }

 ### public static void reverse(){
        int a[]={10,110,42,520,534};
        int i=0;
        int j=a.length-1;
        while(i<j){
            int temp=a[i];
            a[i]=a[j];
            a[j]=temp;
            i++;j--;
        }
        for (int j2 = 0; j2 < a.length; j2++) {
                System.out.print(a[j2]+" ");
        }
    }
   ### public static void removeduplicate(){
        int a[]={10,20,33,50,55,66,77};
        int index=1;
        for(int i=1;i<a.length;i++){
            
            if(a[i]!=a[i-1]){
               
                   a[index]=a[i];
                   index++;
                 
                }
                 
    }
    System.out.println();
    for(int i=0;i<a.length;i++){

          System.out.print(a[i]+" ");
    }        
}
 ##### Generate all the number in increasing order that include{5,6} upto 10 time
  LinkedList i=new LinkedList();
        i.add(5);
        i.add(6); 
        for(int i1=0;i1<10;i1++){
            int cur=(Integer)i.removeFirst();
            if(cur%2==0)
            System.out.println(cur);
            i.add(cur*10+5);
            i.add(cur*10+6);}             
######## public static int max(int a[]){                   ////for finding maximum subarray sum  insimple array not in cirrcularsubbarary   
    int max=a[0];
    int sub=a[0];
    for(int i=1;i<a.length;i++) {
            if( sub+a[i]>a[i]){
                sub=sub+a[i];
                    
            }
    
           
           else{
                 sub=a[i];
           }
           if(max<sub){
            max=sub;}
}
      return max;
}            

##### public static void  csub(){                ///maximum array sum in circular subarray 
                                                             
    int a[]={10,34,10,34,10};                                 //this max function for finding max sum in simple subarray not in circular subrray
    int s=max(a);
    int count=0;
    for(int i=0;i<a.length;i++){
        count=count+a[i];
         a[i]=-a[i];
    }
    int ma=max(a)+count;
    if(s>ma){
          System.out.println(s);
    }
    else{
        System.out.println(ma);
    }
}
########################################## finding kth minimum element with good time complexity##########################################################################
 public static int lumuto(int l,int h){
           int index=l-1;
           int pivot=arr[h];
           for (int i = l; i < h; i++) {
                 if(pivot<arr[i]){
                        index++;
                        int temp=arr[i];
                        arr[i]=arr[index];
                        arr[index]=temp;
                        
                      }
              
           }
         
           int t=arr[index+1];
           arr[index+1]=arr[h];
           arr[h]=t;
          
            return index+1;
         } 
        public static void minelment() {
          int k=3;
          int l=0;
          int h=arr.length-1;
                    while(l<=h){

              int p=lumuto(l,h);
              if(p==k-1){
                     System.out.println(arr[p]);
                     break;
              }
              else if(p>k-1){
                          h=p-1;         
              }
              else{
                        l=p+1;
                        //System.out.println(l);
              }
          }
        }
###### public static void productmax()         //maximum product subbarary
	{
		// your code goes here
		Scanner sc=new Scanner(System.in);
		int arr[]={-6,2,-4,3);
		int max=arr[0];
		int min=arr[0];
	    int output=arr[0];
	    for(int i=1;i<n;i++){
	           if(arr[i]<0){int temp=max;
	           max=min;
	           min=temp;}
	           else if(arr[i]==0){
	               max=0;
	               min=0;
	           }

	           max=Math.max(arr[i],arr[i]*max);
	           min=Math.min(arr[i],arr[i]*min);
	     
	           if(output<max){
	               output=max;
	           }
	    }
	    System.out.println(output);
	}}
###### public static void kmaxsum() {
              int k=3;
              int d=0;
              int max=Integer.MIN_VALUE;
              for (int i = 0; i < k; i++) {
                      d+=arr[i];
              }
              max=d;
              for (int i = k; i < arr.length; i++) {                 
                         d+=arr[i]-arr[i-k];
                         if(d>max){
                           max=d;
                         }
              }
               System.out.println("ksum : "+max);
           }   
          
