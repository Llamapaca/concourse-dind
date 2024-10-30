set:
	fly -t main set-pipeline -p test -c hello.yml
	fly -t main unpause-pipeline -p test
login:
	fly login -u test -p test -c http://concourse:8080 -t main

hijack:
	fly -t main hijack -j test/dind

run:
	fly -t main trigger-job -j test/dind
	fly -t main watch -j test/dind
