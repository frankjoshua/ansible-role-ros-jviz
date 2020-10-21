# ansible-role-ros-jviz [![Build Status](https://travis-ci.org/frankjoshua/ansible-role-ros-jviz.svg?branch=master)](https://travis-ci.org/frankjoshua/ansible-role-ros-jviz)<br>

Deploys a Jviz in a Docker container.

## Requirements

See [requirements.yml](requirements.yml)

## Role Variables

By default we assume that the master is the Robot and use the host ip. This can be changed by setting these variables.

```
ros_ip: "{{ ansible_ssh_host }}"
ros_master_uri: "http://{{ ansible_ssh_host }}:11311"
```

```
docker_name: 'ros_jviz'
port: '8888'
```

## Example Playbook

```
    - hosts: robot
      roles:
         - { role: ansible-role-ros-jviz, ros_master_uri: "http://10.10.10.100:11311" }
```

## Testing

`molecule test`

## License

Apache 2.0

## Author Information

Joshua Frank [@frankjoshua77](https://www.twitter.com/@frankjoshua77)
<br>
[http://roboticsascode.com](http://roboticsascode.com)
