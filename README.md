curl -sL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt-get install -y nodejs

installation iobroker adapter
curl -sLf https://iobroker.net/install.sh | bash -

ordner für adapter erzeugen
mkdir /opt/iobroker/ictb-time/

cd /opt/iobroker/ictb-time/

npx @iobroker/create-adapter@latest

# Basis-Abhängigkeiten für React und Material-UI
alt: npm install react react-dom @material-ui/core @material-ui/icons
npm install @mui/material @emotion/react @emotion/styled
npm install @mui/icons-material


# ioBroker spezifische React-Komponenten
npm install @iobroker/adapter-react

# Eventuelle fehlende Dev-Tools
npm install rimraf

säubern
rm -rf node_modules package-lock.json
npm cache clean --force
npm install



✅ ESLint
✅ Prettier
✅ Code Coverage (optional, aber empfohlen für Tests)
❌ Devcontainer (nur, wenn du Docker verwenden willst)
Willst du direkt mit diesen Einstellungen weitermachen
