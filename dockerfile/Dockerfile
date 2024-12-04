FROM rocker/shiny:4.4

RUN apt-get update \
    && DEBIAN_FRONTEND=noninteractive apt-get install --no-install-recommends --yes \
        ncat \
        vim \
        nano \
        emacs \
        xauth \
        tcl \
        lua5.3 \
        wget \
        ca-certificates \
        curl \
        git

RUN git clone https://github.com/fossw/Clinical_Data_App.git
RUN R -e "install.packages(c('lme4', 'doBy', 'multcomp', 'stringr', 'ggplot2', 'ggpubr', 'plyr', 'dplyr', 'gridExtra', 'ggrepel', 'tidyr', 'ggsignif', 'plotly', 'DT', 'htmltools', 'shinydashboard', 'shinythemes', 'bslib'))"
