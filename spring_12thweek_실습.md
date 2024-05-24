import itertools

def is_prime(n):

    if n <= 1:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

def solution(nums):
    count = 0
 
    for comb in itertools.combinations(nums, 3):
   
        comb_sum = sum(comb)
      
        if is_prime(comb_sum):
            count += 1
    return count

print(solution([1, 2, 3, 4]))
print(solution([1, 2, 7, 6, 4]))
