# nginx-server-block-proxy-tool

A simple tool for managing nginx proxies to node.js applications for different domains and subdomains.

---

### How to use:

`sudo server-blocks new` will create a new nginx server block. You can choose a name (tool internal index), a domain / subdomain and a port that you application is running on. Only localhost is supported at the moment.

`sudo server-blocks edit` allows you to edit existing server blocks. You can change _domain_ and _port_ fields. Eg: `sudo server-blocks edit domain=example.com` or `sudo server-blocks edit port=3000`

`sudo server-blocks delete <name>` will delete a server block by name.

`sudo server-blocks list` will show all server blocks in a table.

`sudo server-blocks -h` shows a help menu similar to this.


### Required Software:

- Certbot (from letsencrypt)
- Nginx
- Node.js

---

_NOTE_ This tool will write directly to `/etc/nginx/sites-available/` and will symlink all enabled sites to `/etc/nginx/sites-enabled/`. The `.nsbpt` tag is added to all files and symlinks generated by this tool.

_**TODO:** https support. (with letsencrypt)_
