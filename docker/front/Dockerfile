FROM node:14.15.3-alpine
 
# 環境変数
ENV LANG C.UTF-8
ENV TZ Asia/Tokyo
ENV APP_HOME /app
ENV PATH ${APP_HOME}/node_modules/.bin:$PATH
ENV HOST 0.0.0.0
ENV PORT 3000
 
WORKDIR ${APP_HOME}
ADD front ${APP_HOME}
 
COPY ../../front/package.json ../../front/yarn.lock $APP/
RUN yarn

EXPOSE 3000
 
CMD ["yarn", "dev"]

