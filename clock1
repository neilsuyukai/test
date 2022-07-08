from apscheduler.schedulers.blocking import BlockingScheduler
import os

sched = BlockingScheduler()

@sched.scheduled_job('cron', day_of_week='mon-sun', hour=8 , minute=30)
def scheduled_job():
	os.system("python push.py")
	print('OK...')
sched.start()
