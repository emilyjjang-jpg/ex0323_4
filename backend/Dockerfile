FROM python:3.9-slim

WORKDIR /code


COPY ./backend/requirements.txt . 
RUN pip install --no-cache-dir -r requirements.txt

# 소스 복사: backend안의 app 폴더를 컨테이너의 /code/app으로 복사 
COPY ./backend/app ./app/

EXPOSE 8000

CMD ["uvicorn","app.main:app","--host","0.0.0.0","--port","8000","--reload"]
