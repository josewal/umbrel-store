FROM node:18-slim

WORKDIR /opt/astrostation

RUN apt-get update && apt-get install -y git && apt-get clean && rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/josewal/astrostation.git .

RUN npm install

RUN npm run build

EXPOSE 4173

# Run the preview command
CMD ["npm", "run", "preview", "--host"]

