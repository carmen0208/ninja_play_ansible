## Play the playbook:

```sh
ansible-playbook nginx.yml -u root -i ../hosts
#PLAY [all] *************************************************************************************************************
#
#TASK [Gathering Facts] *************************************************************************************************
#ok: [10.0.3.73]
#
#TASK [Install nginx] ***************************************************************************************************
#changed: [10.0.3.73]
#
#TASK [Create website directory] ****************************************************************************************
#changed: [10.0.3.73]
#
#TASK [Create main nginx config file] ***********************************************************************************
#changed: [10.0.3.73]
#
#TASK [Create nginx vhost config file] **********************************************************************************
#changed: [10.0.3.73]
#
#TASK [Create websites] *************************************************************************************************
#changed: [10.0.3.73]
#
#TASK [Remove default nginx vhost configuration] ************************************************************************
#changed: [10.0.3.73]
#
#RUNNING HANDLER [restart nginx] ****************************************************************************************
#changed: [10.0.3.73]
#
#PLAY RECAP *************************************************************************************************************
#10.0.3.73                  : ok=8    changed=7    unreachable=0    failed=0
```

```sh
curl http://10.0.3.73/
#<!doctype html>
#
#<html lang="en">
#<head>
#  <meta charset="utf-8">
#  <meta name="description" content="Ansible Overview">
#  <title>Ninja Carmen on ansible</title>
#</head>
#
#<style type="text/css">
#    body {
#      font-size: 16pt;
#      width: 40em;
#      line-spacing: 1.3em;
#      margin: auto;
#      padding: 2em 3em;
#    }
#    #content {
#        padding-left: 2em;
#        border-left: 2px solid black;
#    }
#</style>
#
#<body>
#  <h1>The hope of Ansible.</h1>
#
#  <div id="content">
#      <p>A strong hope; a beautiful hope.</p>
#
#      <p>I <strong>really</strong> hope you configured this server and deployed this website with Ansible, because as this project grows, it will become more and more complicated, and burn you with the fire of a thousand suns if you try to keep using bash for a level of complexity and abstraction that it wasn't designed for.</p>
#
#      <p>Oh, how we laugh, we lucky survivors of the bash/Perl era. How we laugh, desperately, with tears in our eyes, seeking understanding for all the horror we've seen.</p>
#
#    </div>
#
#</body>
```
