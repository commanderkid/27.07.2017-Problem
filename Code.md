# http://www.codeabbey.com/index/task_view/combinations-counting

#-------------------------------------------------------------------------------
# Name:        module1
# Purpose:
#
# Author:      Pushkin-AA
#
# Created:     27.10.2017
# Copyright:   (c) Pushkin-AA 2017
# Licence:     <your licence>
#-------------------------------------------------------------------------------

def function(N, K):

    i, j = 0, 1
    while i < N:
        i = i + 1
        j = j * i

    i, g = 0, 1
    while i < K:
        i = i + 1
        g = g * i

    i, l = 0, 1
    while i < (N - K):
        i = i + 1
        l = l * i

    return int(j / (g * l))


per = int(input())
obsh = []
for i in range(per):
    resh = [int(i) for i in input().split()]
    resh = function(resh[0], resh[1])
    obsh.append(str(resh))
print(" ".join(obsh))
