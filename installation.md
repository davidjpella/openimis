# Installation procedures 

Clone docker version
```ssh
git clone https://github.com/openimis/openimis-dist_dkr.git && cd openimis-dist_dkr
```

Create virtual environment by run the following commands 
```ssh
python3.10 -m venv env && source env/bin/activate
```

## For the backend

Install python3.10 (If not installed)
```ssh
brew install python@3.10
```

Clone backend project `openimis-be_py`
```ssh
git clone https://github.com/openimis/openimis-be_py.git && cd openimis-be_py
```

Install dependencies 
```ssh
cd openIMIS && pip install -r requirements.tx
```

Generate openIMIS modules 
```ssh
cd ../scripts && python modules-requirements.py ../openimis.json > modules-requirements.txt
```

Install openIMIS current modules
```ssh
cd ../openIMIS && pip install -r modules-requirements.txt
```

Copy the example environment setup and adjust the settings
```ssh
cd .. && cp .env .env.example
```

Start openIMIS from within(to see if everything is working correctly)
```ssh
cd openIMIS && python manage.py runserver
```

### After everything go to project root directory (docker version) 

Change permissions of `deploy_openimis.sh` to executable 
```ssh
chmod +x deploy_openimis.sh
```

Run the followimng command start services
```ssh
./deploy_openimis.sh
```
