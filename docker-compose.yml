version: '3.4'

volumes:
  postgres_data:
  pgadmin:
  
services:
  postgres:
    image: postgres:latest
    volumes:
      - postgres_data:/var/lib/postgresql/data/
    ports: 
      - "5432:5432"   
    environment:
      POSTGRES_USER: testgres
      POSTGRES_PASSWORD: testgres
  
  pgAdmin4:
    image: dpage/pgadmin4
    restart: always
    ports:
      - 5050:80
    volumes:
      - pgadmin:/root/.pgadmin
    environment:
      PGADMIN_DEFAULT_EMAIL: test@test.de
      PGADMIN_DEFAULT_PASSWORD: testgres
    depends_on:
      - postgres
