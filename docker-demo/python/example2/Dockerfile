FROM python:3.8

WORKDIR /app

COPY main.py .

RUN pip install uvicorn
RUN pip install fastapi


ENTRYPOINT ["python"]

CMD ["main.py"]

