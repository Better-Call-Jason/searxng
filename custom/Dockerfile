FROM searxng/searxng:latest

USER root

# Copy custom logo files
COPY custom/img/searxng.png /usr/local/searxng/searx/static/themes/simple/img/searxng.png
COPY custom/img/searxng.svg /usr/local/searxng/searx/static/themes/simple/img/searxng.svg

# Copy custom template
COPY custom/templates/simple/base.html /usr/local/searxng/searx/templates/simple/base.html

# Fix permissions
RUN chown -R searxng:searxng /usr/local/searxng/searx/static/themes/simple/img/ && \
    chown -R searxng:searxng /usr/local/searxng/searx/templates/simple/base.html

USER searxng
