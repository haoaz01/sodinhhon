# sohuahon
import random

def find_promise_pair():
    while True:
        m = random.randint(1, 1000)
        n = random.randint(1, 1000)
        
        if sum_divisors(m) == n + 1 and sum_divisors(n) == m + 1:
            return (m, n)

def sum_divisors(num):
    divisors = []
    for i in range(1, num):
        if num % i == 0:
            divisors.append(i)
    return sum(divisors)

m, n = find_promise_pair()
print("Cặp số hứa hôn ngẫu nhiên là:", (m, n))
