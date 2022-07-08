# read from cpe.json

import json

with open('cpe.json','r') as f:
	response = json.load(f)

# print(response[0])
import random
point   = random.randrange(0,len(response))


#for i in range(len(response)):
#	if(i[0])
#print(response[200][0])


head = response[point][:-2]
#print('last two: '+head)
url     = 'https://uva.onlinejudge.org/external/'+head+'/'+response[point]+'.pdf'
#print(url)
context = 'click me: \n' + url
print(context) 
import smtplib
from email.mime.text import MIMEText

user = "程式小老師"
pwd  = "終極密碼"
msg = MIMEText(context)
msg['Subject'] = '每日一題'
msg['From'] = user
#msg['To'] = 'letitia850723@gmail.com'
msg['To'] = 'receiver_1,receiver_2...'

server = smtplib.SMTP_SSL('smtp.gmail.com',465)
server.ehlo()
server.login(user,pwd)
server.send_message(msg)
server.quit()

print('Email sent!')
