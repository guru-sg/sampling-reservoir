# sampling-reservoir
to implement sampling reservoir algorithm

                    import java.util.*; 
                    public class Main
                    {
                      public static void main(String[] args) { 
                      Scanner sc = new Scanner(System.in);
                      int i;
                      int n = sc.nextInt();
                      //getting elements of infinitely large array
                      int sample[] = new int[n];
                      for (i = 0; i < n; i++)
                      {
                          sample[i] = sc.nextInt();
                      }
                      //no.of random elements to be fetched
                      int k = sc.nextInt(); 
                      // new array to store randomly selected elements
                      int result[] = new int[k];
                      for (i = 0; i < k; i++) 
                      {
                          result[i] = sample[i]; 
                      }
                      Random r = new Random(); 
                      for (i = k; i < n; i++) 
                      { 
                          int j = r.nextInt(i + 1); 
                          if(j < k) 
                            result[j] = sample[i];			 
                      } 
                      System.out.println("The randomly selected elements fr om resultant array:");
                      for (i = 0; i<result.length; i++)
                      {
                          System.out.println(result[i]);
                      }
                     } 
                   } 


