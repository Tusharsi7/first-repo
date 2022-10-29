#array spiral matrix
trying to creat firse repo from pw skills

 public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int m = sc.nextInt();
        int[][] matrix = new int[n][m];


        for(int i =0; i<n; i++){
            for(int j=0; j<m; j++){
                matrix[i][j]= sc.nextInt();
            }
        }

        System.out.println("the sprial matrix is ;-");
        int rowstart=0;
        int rowend=n-1;
        int colstart=0;
        int colend=m-1;


        while(rowstart<=rowend && colstart <= colend){

            //1

            for(int i=colstart; i<=colend; i++){
                System.out.print(matrix[rowstart][i] + " ");
            }
            rowstart ++;

            //2

            for(int j=rowstart; j<=rowend; j++){
                System.out.print(matrix[j][colend] + " ");
            }
            colend --;

            //3

            for (int i=colend; i>=colstart ; i--){
                System.out.print(matrix[rowend][i] + " ");
            }
            rowend--;

            //4


            for(int j=rowend; j>=rowstart; j--){
                System.out.print(matrix[j][colstart]+ " ");
            }
            colstart++;
            System.out.println();

        }

    }
