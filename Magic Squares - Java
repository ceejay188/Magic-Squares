package com.company;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        //Magic Square Project
        Scanner input = new Scanner(System.in);
        int n, magic_no, k = 1, tracker = 1;
        System.out.print( "\t\t\t********************   THE MAGIC SQUARE  ********************\n"+
                "A Magic Square is one which has a perfect sum and equal number of rows and columns.\n"+
                "The numbers in every row, column and the 2 longest diagonals always add up to the perfect sum.\n"+
                "The perfect sum can also be called the Magic Number.\n"+
                "This program generates a perfect Magic Square.\n"+
                "A perfect Magic Square is only possible with odd numbers of rows and infinite possibilities.\n"+
                "The Magic Number of a perfect Magic Square must be divisible by the number of rows in the Square.\n\n\n"+
                "Let's get started.\nInput your number of rows."+
                " For just this example,\n"+
                "(i.e we can achieve much greater), and purposes of neatness,\n"+
                "it must be an odd number greater than 1 and less than 26.\nRows:\t");
        n = input.nextInt();
        magic_no = ((n * ((n * n) + 1)) / 2); // Obtaining Magic Number
        int i = 0, j = ((n - 1) / 2); // Initializing the number '1' position.
        int[][] m_square = new int[100][100];
        int[][] R = new int[1000][1000];

        //************Working out the Math.
        //************Generating the numbers of the grid.
        for (int itr = 0; itr < (n*n); itr++)
        {
            R[itr][0] = k;
            k++;
        }
        k = 1; // Making sure the sequence of numbers is in the right order.

        //Filling out the Magic Square.
        m_square[0][((n - 1) / 2)] = 1;
        while (tracker != (n * n))
        {
            if ((i == 0 && j == (n - 1)) || (i == (n - 2) && j == 0)) // Z
            {
                i++;
                m_square[i][j] = R[k][0];
                k++;
                tracker++;

            }
            else if (i == (n - 1) && j == ((n - 1) / 2)) // L
            {
                m_square[i][j] = (n*n);
                tracker++;

            }
            else if (i == 0 && j < (n - 1)) // B
            {
                i = (n - 1); j++;
                m_square[i][j] = R[k][0];
                k++;
                tracker++;

            }
            else if (i > 0 && j == (n - 1) && i < n) // A
            {
                i--; j = 0;
                m_square[i][j] = R[k][0];
                k++;
                tracker++;

            }
            else if ((i == (n - 1) && j < (n - 1) && j != ((n - 1) / 2)) || (j == 0 && i > 0 && i != (n - 2))) // Ticked area
            {
                i--; j++;
                m_square[i][j] = R[k][0];
                k++;
                tracker++;

            }
            else if (i > 0 && j > 0 && j < (n - 1) && i < (n - 1)) // Shaded region
            {
                i--; j++;
                if(m_square[i][j] < R[k][0] && m_square[i][j] > 0) // Occupied box
                {
                    i += 2; j--;
                }
                // Unoccupied box
                m_square[i][j] = R[k][0];
                k++;
                tracker++;
            }
        }

        //************Printing out the magic square.
        System.out.print("Your Magic Square has a Magic Number.\nThe Magic Number is " + magic_no +".\n\nYour Magic Square is a " +
                n + "x" + n + " Magic square with a Magic Number of " + magic_no + ".\n\n\t\t");
        for (int i2 = 0; i2 < n; i2++)
        {
            for (int j2 = 0; j2 < n; j2++)
            {
                System.out.print( " " + (m_square[i2][j2]));
            }
            System.out.print( "\n\t\t");
        }
    }
}
