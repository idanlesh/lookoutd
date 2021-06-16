How to run the project:

1. Run sonarcheck-analyzer:
	a. apt-get install libxml2-dev -y
	b. pip3 install -r requirements.txt
	c. python3 sonarcheck_analyzer.py
2. Run docker-compose:
	a. docker-compose -f docker-compose.yml up -d --force-recreate bblfsh postgres
3. Run lookoutd:
	a. ./lookoutd migrate --db postgres://postgres:postgres@il-linubvm-205:15432/lookout?sslmode=disable
	b. ./lookoutd serve --db=postgres://postgres:postgres@il-linubvm-205:15432/lookout?sslmode=disable

Based on below sites:
	https://github.com/src-d/lookout
	https://github.com/src-d/lookout/blob/master/docs/how-to-run.md
	https://github.com/src-d/lookout/blob/master/docs/configuration.md
	https://github.com/bblfsh/sonar-checks
	https://github.com/src-d/lookout-sonarcheck-analyzer
