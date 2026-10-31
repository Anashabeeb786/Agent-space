FROM node:22-alpine

WORKDIR /app

COPY . .

# Remove local runtime state and secrets
RUN rm -f config.json memory-history.json agent-space.db agent-space.db-shm agent-space.db-wal || true

ENV PORT=18790
ENV BIND_HOST=0.0.0.0

EXPOSE 18790

CMD ["node", "server.js", "--demo"]