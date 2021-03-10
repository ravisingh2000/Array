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
