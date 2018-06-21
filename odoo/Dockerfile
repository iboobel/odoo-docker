FROM odoo:10.0

USER root

COPY ./odoo.conf /etc/odoo/odoo.conf
RUN chown odoo:odoo -R /etc/odoo/

RUN pip install xlrd

USER odoo