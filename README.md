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
    }
