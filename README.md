# **ASSIGNMENT 3**

  Student ID :700749050
  
  Assignment by : Meghana Chodagiri
  
  Course: CS5710
  
  CRN Number: 232922
  
  GitHub Link: https://github.com/meghanach1/Assignment3

  VideoLink:
  https://drive.google.com/file/d/1zM28Ex6ydlhaxkqF-BHBR3L8uDQZ6XiF/view?usp=share_link
  
  
   1. Numpy:
    
   a. Using NumPy create random vector of size 15 having only Integers in the range 1-20.
    
   1. Reshape the array to 3 by 5
    
   2. Print array shape.
   3. Replace the max in each row by 0

    A.  In this problem, I have created a random array using rand function with integer range 1-20 and size 15. Then reshape the array using reshape function and printed the shape using shape function then using the maxNum and rand replaced the max value with 0.
    import numpy as np
     using randint method, creating random vector of size 15 within range 1 and 20
    x = np.random.randint(1,20, size = 15)
    print (x)

   Below is the output:
     
     [ 7 12 19  8  3 19 18 18 14 16 11  4  7  8 19]

 
   1. Reshape the array to 3 by 5

    For reshaping the array, using reshape() method
    y=x.reshape(3,5)
    print(y)

 

Output:

    [[ 7 12 19  8  3]
     [19 18 18 14 16]
     [11  4  7  8 19]]


# 2. Print array shape.

  
    print ("array is :",y)
    #using array. shape to print the shape of the array
    print ("array shape is:",y.shape)
 
Output:
  
     array is: [[ 7 12 19 8  3]
     [19 18 18 14 16]
     [11 4  7  8 19]]
    array shape is: (3, 5)

 3. Replace the max in each row by 0

  
        new_a = np.where(y == [
          [i]
          for i in np.amax(y, axis = 1)
        ], 0, y)

        print(new_a)
 
Output:

    [[ 0 12  5  4 10]
     [14 12  4  0  6]
     [ 7  4  0  5 12]]

2. Create a 2-dimensional array of size 4 x 3 (composed of 4-byte integer elements), also print the shape, type, and data type.
of the array.

     A. In this problem I have printed the array using array function with 4- byte integer elements. I have printed the shape of array using shape function and type using the type function then using the data type function printed the data type.
          import numpy as np

# create a 2-dimensional array of size 4x3

  arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]], dtype=np.int32)

# print the array shape using array.shape

  print("Array shape:", arr.shape)

# print the array type using type()

  print("Array type:", type(arr))

# print the array data type using dtype

  print("Array data type:", arr.dtype)
 
Output:

    Array shape: (4, 3)
    Array type: <class 'numpy.ndarray'>
    Array data type: int32

b. Write a program to compute the eigenvalues and right eigenvectors of a given square array given below:
[[ 3 -2]
[ 1 0]]

    A.In this program, I have defined the array using array function then computed the diagonal elements using diagonal sum and trace() then print the sum of diagonal using print() function.
    import numpy as np

# define the square array
    A = np.array([[3, -2], [1, 0]])

# compute the eigenvalues and right eigenvectors
    eigenvalues, eigenvectors = np.linalg.eig(A)

# print the eigenvalues and right eigenvectors
    print("Eigenvalues:", eigenvalues)
    print("Right eigenvectors:")
    print(eigenvectors)
 
Output:

    Eigenvalues: [2. 1.]
    Right eigenvectors:
    [[0.89442719 0.70710678]
     [0.4472136  0.70710678]]

c. Compute the sum of the diagonal element of a given array.
[[0 1 2]
[3 4 5]]

    import numpy as np

    # define the array
    A = np.array([[0, 1, 2], [3, 4, 5]])

    # compute the sum of the diagonal elements
    diagonal_sum = np.trace(A)

    # print the sum of the diagonal elements
    print("Sum of diagonal elements:", diagonal_sum)

 
Output:

  Sum of diagonal elements: 4

d. Write a NumPy program to create a new shape to an array without changing its data.
Reshape 3x2:
[[1 2]
[3 4]
[5 6]]
Reshape 2x3:
[[1 2 3]
[4 5 6]]
A. 

    import numpy as np

    # define the original array
    arr = np.array([[1, 2], [3, 4], [5, 6]])

    # reshape to 3x2
    arr_3x2 = arr.reshape(3, 2)

    # reshape to 2x3
    arr_2x3 = arr.reshape(2, 3)

    print("Reshaped to 3x2:\n", arr_3x2)
    print("Reshaped to 2x3:\n", arr_2x3)


Output:

    Reshaped to 3x2:
     [[1 2]
     [3 4]
     [5 6]]
    Reshaped to 2x3:
     [[1 2 3]
     [4 5 6]]

2. Matplotlib
1. Write a Python programming to create a below chart of the popularity of programming Languages.
 Sample data:
Programming languages: Java, Python, PHP, JavaScript, C#, C++
Popularity: 22.2, 17.6, 8.8, 8, 7.7, 6.7

    A In this problem, I have first defined the programming languages and their
    popularity as lists using Python. I have used the plt.pie() method from Matplotlib to
    create a pie chart. I then used the plt.axis() method to set the chart and I used the
    plt.show() method to display the chart.

    import matplotlib.pyplot as plt
    # Data to plot
    languages = 'Java', 'Python', 'PHP', 'JavaScript', 'C#', 'C++'
    popularity = [22.2, 17.6, 8.8, 8, 7.7, 6.7]
    colors = ["#1f77b4", "#ff7f0e", "#2ca02c", "#d62728", "#9467bd", "#8c564b"]
    # explode 1st slice
    explode = (0.1, 0, 0, 0,0,0)  
    # Plot
    plt.pie(popularity, explode=explode, labels=languages, colors=colors,
    autopct='%1.1f%%', shadow=True, startangle=140)

    plt.axis('equal')
    plt.show()


Output:

 
<img width="258" alt="image" src="https://user-images.githubusercontent.com/122816638/229264113-22024fb8-4318-40b5-961c-2f7e426f80fc.png">

