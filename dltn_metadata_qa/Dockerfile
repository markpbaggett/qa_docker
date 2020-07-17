FROM python:3.8.4
WORKDIR /qa
RUN echo "Installing extras."
RUN apt-get update && apt-get install -y git
RUN echo "Cloning DLTN Metadata QA" && git clone --progress http://github.com/markpbaggett/dltn_metadata_QA.git qa
RUN cd qa && pip install --upgrade pip && pip install pipenv && pipenv install
