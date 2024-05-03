FROM python:3.8-slim-buster

WORKDIR python_38
COPY requirements.txt requirements.txt
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

CMD ["jupyter", "lab", "--ip","0.0.0.0","--allow-root", "--no-browser"]
