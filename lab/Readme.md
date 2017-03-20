## Configuring test environment with Ansible
------------------------------------------------------------------------------

- Requires Ansible 2.1
- Expects CentOS/RHEL 7 hosts

### Deployment Example

The inventory file looks as follows:

Version0.1  Configure all test servers as web server.

		#The site wide list of web servers
		[webservers]
		webserver1
        webserver2

		#The list of database servers
		#[dbservers]
		#dbserver1
        #dbserver2

		#The list of load balancer servers
		#[lbservers]
		#loadbalancer1


Configure the site with the following command:

		ansible-playbook -e 'host_key_checking=False' -i hosts site.yml
