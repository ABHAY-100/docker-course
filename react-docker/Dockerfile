FROM node:20-alpine
RUN addgroup -S app && adduser -S -G app app
WORKDIR /app
COPY --chown=app:app package*.json ./
RUN npm install
COPY --chown=app:app . .
RUN chown -R app:app /app
USER app
EXPOSE 5173
CMD npm run dev