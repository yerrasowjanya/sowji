# sowji
// C# Program for Bankers Algorithm  using System;  using System.Collections.Generic;  class GFG  {  static int n = 5; // Number of processes  static int m = 3; // Number of resources  int [,]need = new int[n, m];  int [,]max;  int [,]alloc;  int []avail;  int []safeSequence = new int[n];  void initializeValues()  {  // P0, P1, P2, P3, P4 are the Process  // names here Allocation Matrix  alloc = new int[,] {{ 0, 1, 0 }, //P0  { 2, 0, 0 }, //P1  { 3, 0, 2 }, //P2  { 2, 1, 1 }, //P3  { 0, 0, 2 }};//P4  // MAX Matrix  max = new int[,] {{ 7, 5, 3 }, //P0  { 3, 2, 2 }, //P1  { 9, 0, 2 }, //P2  { 2, 2, 2 }, //P3  { 4, 3, 3 }};//P4  // Available Resources  avail = new int[] { 3, 3, 2 };  }  void isSafe()  {  int count = 0;  // visited array to find the  // already allocated process  Boolean []visited = new Boolean[n];  for (int i = 0; i &lt; n; i++)  {  visited[i] = false;  }  // work array to store the copy of  // available resources  int []work = new int[m];  f
// C# Program for Bankers Algorithm 
using System; 
using System.Collections.Generic; 
class GFG 
{ 
static int n = 5; // Number of processes 
static int m = 3; // Number of resources 
int [,]need = new int[n, m]; 
int [,]max; 
int [,]alloc; 
int []avail; 
int []safeSequence = new int[n]; 
void initializeValues() 
{ 
// P0, P1, P2, P3, P4 are the Process 
// names here Allocation Matrix 
alloc = new int[,] {{ 0, 1, 0 }, //P0 
{ 2, 0, 0 }, //P1 
{ 3, 0, 2 }, //P2 
{ 2, 1, 1 }, //P3 
{ 0, 0, 2 }};//P4 
// MAX Matrix 
max = new int[,] {{ 7, 5, 3 }, //P0 
{ 3, 2, 2 }, //P1 
{ 9, 0, 2 }, //P2 
{ 2, 2, 2 }, //P3 
{ 4, 3, 3 }};//P4 
// Available Resources 
avail = new int[] { 3, 3, 2 }; 
} 
void isSafe() 
{ 
int count = 0; 
// visited array to find the 
// already allocated process 
Boolean []visited = new Boolean[n]; 
for (int i = 0; i < n; i++) 
{ 
visited[i] = false; 
} 
// work array to store the copy of 
// available resources 
int []work = new int[m]; 
f
