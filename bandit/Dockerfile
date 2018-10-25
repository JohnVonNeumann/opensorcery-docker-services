FROM python:alpine

# So I know pinning versions is a best practice, but at this current moment in
# time I really don't think this is a big enough problem to spend more time on
# playing around with automation to pin versions in an intelligent way.
# hadolint ignore=DL3013
RUN pip3 install bandit

WORKDIR /code

ENTRYPOINT ["bandit"]
