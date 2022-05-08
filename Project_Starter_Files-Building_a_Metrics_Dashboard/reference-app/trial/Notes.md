# Additional Notes

To run services manually from their respective directories:

```
pip list

# cleanup
pip uninstall -y -r >(pip freeze)

# install dependencies
pip install -r requirements.txt

# run app
gunicorn --access-logfile - --error-logfile - -w 4 -b 0.0.0.0:8082 app:app
```

Alternatively, you can use the docker image to run the app:

```
docker run --rm -p 8082:8080 -it barbietunnie/observability-backend-service
```