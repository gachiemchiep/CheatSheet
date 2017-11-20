Installation
------------------------

.. code-block:: sh

  # Install
  sudo apt-get install rabbitmq-server
	sudo systemctl enable rabbitmq-server
	
  # Start
  sudo rabbitmq-server 
	
  # Check status
	rabbitmqctl status

	# Enable web interface
	sudo rabbitmq-plugins enable rabbitmq_management
	http://10.72.222.97:15672/

	# Create XXX user as root user
	sudo rabbitmqctl add_user user_XXX user_password
	sudo rabbitmqctl set_user_tags user_XXX administrator
	sudo rabbitmqctl set_permissions -p / user_XXX ".*" ".*" ".*"

Userful command
-------------------------

.. code-block:: sh

  # List message queue
  rabbitmqadmin list queues name

  # Clear message from queue
  sudo rabbitmqctl purge_queue queue_name

  rabbitmqctl list_vhosts
  rabbitmqctl list_queues -p <vhost>

  rabbitmqctl cluster_status

  rabbitmqctl stop_app
  rabbitmqctl join_cluster <node>
  rabbitmqctl start_app

  rabbitmqctl report    # Dump detailed report on RabbitMQ instance  

  # Plugin management
  /usr/lib/rabbitmq/bin/rabbitmq-plugins enable <name>
  /usr/lib/rabbitmq/bin/rabbitmq-plugins list   

  # Live modifications using eval
  rabbitmqctl eval 'application:set_env(rabbit, reverse_dns_lookups, true).'
