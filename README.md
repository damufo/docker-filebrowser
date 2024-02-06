# Installation

## Setting general configuration
```
git clone https://github.com/damufo/docker-filebrowser.git
cd docker-filebrowser
cp sample.env .env
sed -i "s/siteaddress/filebrowser.your-domain.org/g" .env
```
## Setting user id
Get user id
```
id -u
```
With command "id" you get user id to set in .env file.
If distinct of 1000

sed -i "s/1000/user_id/g" .env
```

## Setting data folder
```
sed -i "s+/home/user/data_folder/+/home/your_user/data_folder/+g" .env
touch filebrowser.db
```

## Start site

```
docker-compose -f docker-compose.yml -f docker-compose.traefik.yml up -d
docker-compose logs -f
```

Forked from @atareao (Lorenzo)
