FROM node:alpine AS development

WORKDIR /usr/src/app

COPY package.json ./
COPY package-lock.json ./
COPY tsconfig.json tsconfig.json

# RUN npm cache clean --force
RUN npm install npm@8.11.0 -g
RUN npm cache clear -f
RUN npm i
# RUN npm i --loglevel verbose

# COPY . .
COPY apps/auth apps/auth
COPY libs libs

RUN cd apps/auth && npm install

RUN npm run build

FROM node:alpine AS production

ARG NODE_ENV=production
ENV NODE_ENV=${NODE_ENV}

WORKDIR /usr/src/app

COPY package.json ./
COPY package-lock.json ./

# RUN npm cache clean --force
RUN npm install npm@8.11.0 -g
RUN npm cache clear -f
RUN npm i
# RUN npm i --loglevel verbose

COPY --from=development /usr/src/app/dist ./dist

CMD ["node", "dist/apps/auth/main"]
