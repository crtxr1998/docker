FROM node
ENV appPath /app
ADD . ${appPath}
WORKDIR ${appPath}
RUN npm config set registry https://registry.npm.taobao.org && npm i
ONBUILD RUN  echo "......trigger parent image Obuild...... ${date}" > ${appPath}/build.txt
VOLUME [ "${appPath}/" ]
EXPOSE 8081
ENTRYPOINT [ "npm" ]
CMD  [ "npm start" ]