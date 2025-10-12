13. Roman to Integer
def romanToInt(s: str) -> int:
    roman_map = {
        'I': 1, 'V': 5, 'X': 10,
        'L': 50, 'C': 100, 'D': 500, 'M': 1000
        }
    incorrect = []
    for i in list(s):
        if i not in roman_map:
            incorrect.append(i)


    if len(incorrect) == 0:
        total = 0
        prev = 0
        a = list(s)
        for i in reversed(a):
            if prev <= roman_map[i]:
                total += roman_map[i]
            else:
                total -= roman_map[i]
            prev = roman_map[i]    
        return total
    else:
        print("you cant use this letters/signs: ", incorrect)
        
while True:
    a = input("Write roman numbers: ")
    print("Sum of roman numbers: ", romanToInt(a))



class Solution:
    def romanToInt(self, s: str) -> int:
        roman_map = {
            'I': 1, 'V': 5, 'X': 10,
            'L': 50, 'C': 100, 'D': 500, 'M': 1000
            }
        total = 0
        prev = 0
        a = list(s)

        for i in reversed(a):
            if prev <= roman_map[i]:
                total += roman_map[i]
            else:
                total -= roman_map[i]
            prev = roman_map[i]    
        return total
