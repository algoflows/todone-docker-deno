FROM denoland/deno:1.10.3

RUN deno install -qAf --unstable https://deno.land/x/denon/denon.ts

WORKDIR /app
ADD . .

COPY deps.ts .
RUN deno cache --unstable deps.ts

ADD . .
