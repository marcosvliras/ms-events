COV_THRESHOLD := 80

test:
	rm -rf .pytest_cache __pycache__ htmlcov coverage.xml .coverage
	uv run python -m pytest --cache-clear
	uv run python -m pytest --cov=ms-events --cov-report xml:coverage.xml --cov-report term-missing --cov-report html --cov-fail-under=$(COV_THRESHOLD)