import datetime
import requests

def check_internet():
    """检查网络连接是否正常。"""
    try:
        requests.get('http://google.com', timeout=3)
        return True
    except requests.RequestException:
        return False

def log_status(status):
    """记录检查时间和网络状态到日志文件。"""
    with open('internet_status_log.txt', 'a') as log_file:
        timestamp = datetime.datetime.now().strftime('%Y-%m-%d %H:%M:%S')
        log_file.write(f'{timestamp} - Internet Status: {"Connected" if status else "Disconnected"}\n')

if __name__ == '__main__':
    status = check_internet()
    log_status(status)
