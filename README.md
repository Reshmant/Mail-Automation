# Mail-Automation
'''This code sends the mail/msg to the destination mail id.
You can even send the mail anonymously which isn't recommended coz you may get into problems.
You can try it with your friends though :P'''
import email
import smtplib
import imaplib
import getpass
unm = input("enter your Email : ")
pwd = getpass.getpass("enter password : ")
unmd = input("enter your Email : ")
msg='Hey there!!'
server=smtplib.SMTP('smtp.gmail.com:587')
server.starttls()
server.login(unm,pwd)
server.sendmail(unm,unmd,msg)
server.quit()
