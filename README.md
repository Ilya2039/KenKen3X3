# KenKen3X3

# Решение ken ken 3*3

import random
def printMatrix ( matrix ):
   for i in range ( len(matrix) ):
      for j in range ( len(matrix[i]) ):
          print ( "{:4d}".format(matrix[i][j]), end = "" )
      print ()


matrix = [[1, 0, 0],
    [1, 2, 0],
    [0, 0, 3]]
#c = [r[1] for r in matrix]
#print(len(set(c)))
#print(c)
a1 = 0
a2 = 0
b0 = 0
b1 = 0
c0 = 0
c1 = 0
while abs(matrix[0][1] - matrix[0][2]) != 1 or abs(matrix[1][0] - matrix[1][1]) != 1 or matrix[2][0] + matrix[2][1] != 5 or \
        matrix[1][2] * matrix[2][2] != 3 or len(set(matrix[:][0])) != 3 or len(set(matrix[:][1])) != 3 or \
        len(set(matrix[:][2])) != 3 or len(set(c0)) != 3 or len(set(c1)) != 3 or len(set(c2)) != 3:
    matrix[0][0] = 1
    matrix[0][1] = random.randint(1, 3)
    matrix[0][2] = random.randint(1, 3)
    matrix[1][0] = random.randint(1, 3)
    matrix[1][1] = random.randint(1, 3)
    matrix[2][0] = random.randint(1, 3)
    matrix[2][1] = random.randint(1, 3)
    matrix[1][2] = random.randint(1, 3)
    matrix[2][2] = random.randint(1, 3)
    c0 = [r[0] for r in matrix]
    c1 = [r[1] for r in matrix]
    c2 = [r[2] for r in matrix]
#print(matrix)

printMatrix(matrix)
