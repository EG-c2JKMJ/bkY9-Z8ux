import requests, json

def get_json(url,username,password):
    response = requests.get(
        url,
        auth=requests.auth.HTTPBasicAuth(username,password))
    print(url)
    for item in json.loads(response.text):
        if (item['directory']):
            get_json(
                url + "/" + item['name'],
                username,
                password
            )
        else:
            print(url + "/" + item['name'])

    return


url = 'https://api.orls.voxeo.net/files'
username = 'SSA_PCI_SomeAccountName'
password = 'thispasswordisterrible'

get_json(url,username,password)
