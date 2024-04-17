# python-ip-logger

this is a python ip logger that i made, im a newbie so this is just a shitty ip logger i will try to upgrade it.

First, install the requests library if you haven't already:
pip install requests

Ip logger:

import requests

def handle_client(client):
    client.send(b'Welcome to the IP logger!')
    ip_addr = get_client_ip(client)
    print(f'[+] {ip_addr} connected.')

    # Send a POST request to your webhook
    webhook_url = "https://your-webhook-url.com"
    data = {"ip_address": ip_addr}
    requests.post(webhook_url, json=data)

    client.send(f'Your IP address is: {ip_addr}'.encode())
    client.close()
Replace "https://your-webhook-url.com" with your actual webhook URL.
Now, your Python IP logger will send the IP addresses to your webhook

edit:github doesnt even put it right lmao

