import requests

# GitHub repository information
owner = 'your_username'
repo = 'your_repository'
package_name = 'your_package_name'
token = 'your_github_token'

# Retrieve information about the latest version of the package
package_url = f'https://api.github.com/repos/{owner}/{repo}/packages/{package_name}/versions/latest'
headers = {'Authorization': f'token {token}'}
response = requests.get(package_url, headers=headers)
package_data = response.json()

# Extract Docker image digest from the package metadata
docker_digest = package_data['metadata']['docker']['digest']

# Update repository metadata to include information about the linked package
repository_metadata_url = f'https://api.github.com/repos/{owner}/{repo}'
repository_metadata = {
    'name': repo,
    'owner': {
        'login': owner
    },
    'package': {
        'name': package_name,
        'docker_digest': docker_digest
    }
}
response = requests.patch(repository_metadata_url, headers=headers, json=repository_metadata)

# Check response status to ensure the update was successful
if response.status_code == 200:
    print('Package linked to repository successfully.')
else:
    print('Failed to link package to repository.')
