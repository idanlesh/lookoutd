How to run the project:

1. Run sonarcheck-analyzer:
	a. cd lookout-sonarcheck-analyzer/
	b. apt-get install libxml2-dev -y
	c. pip3 install -r requirements.txt
	d. python3 sonarcheck_analyzer.py
2. Run docker-compose:
	a. docker-compose -f docker-compose.yml -f docker-compose-rabbitmq.yml up -d --force-recreate bblfsh postgres rabbitmq
3. Run lookoutd:
	a. ./lookoutd migrate --db postgres://postgres:postgres@il-linubvm-205:15432/lookout?sslmode=disable
	b. ./lookoutd serve --db=postgres://postgres:postgres@il-linubvm-205:15432/lookout?sslmode=disable
