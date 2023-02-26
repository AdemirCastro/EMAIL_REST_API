
# EMAIL REST API

Containerized Restful API for email management, made for production. The API was made with FastAPI and built-in Python libs, and is deployed by a Docker container based on Alpine, a lightweight Linux distro.

## Features
With this API, we have the following features:
- Get email messages
- Reply email messages
- Send email messages
- Forward email messages
- Delete email messages
- Get mailboxes
- Rename mailboxes
- Create mailboxes
- Delete mailboxes
- Get email messages UIDs
- Move email messages between mailboxes


## Requirements

To create and deploy the container with the API running, you only need [Docker](https://www.docker.com/).
## Documentation

All the microservice features and documentation can be accessed in the link: [Email API Documentation](https://ademircastro.github.io/EMAIL_REST_API/)

For a more detailed documentation, generated by Swagger, you can access the API URL on the endpoint /docs. By exemple: 
```
localhost:8000/docs
```

## Deployment

To deploy the API, you must first generate the Docker image, and then start the container. Just run the following bash commands as super user (sudo) on repository folder:

```bash
docker build -t email-api-image .
```
```bash
docker run -p 8000:8000 --name email-api email-api-image
```

This second commmand create and run the container running the APi in the port 8000. To deploy the API in another port, you must run the bash command as super user (sudo) on the repository folder:
```bash
docker run -p [port]:8000 --name email-api email-api-image
```


## License

[MIT License](https://choosealicense.com/licenses/mit/)
Copyright (c) 2023 Ademir dos Santos Castro

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
