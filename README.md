s = 'cgrylgnd'

myStr = ''

largestStr = ''

integer = 0

for count in range(1,len(s)):
    
    if s[count]>=s[count-1]:
        myStr += s[count-1]
        integer += 1
        if count == len(s) -1:
            myStr += s[count]
            if len(myStr)>len(largestStr):
                largestStr = myStr
        if len(myStr) == len(s):
            largestStr = myStr
    else:
        if integer >0:
            myStr += s[count -1]
            if len(myStr)>len(largestStr):
                largestStr = myStr
            integer = 0
            myStr = ''

if largestStr == '':
    
    largestStr = s[0]
 
print (largestStr)
        
    
