.. _nifi_datstore_services:

Data Store Services
-------------------

GeoMesa processors require a ``DataStoreService`` to connect to the back-end data source. To use a controller services,
first add one to the workspace and then configure its properties tab. The following data stores are available in GeoMesa:

HBase
~~~~~

The ``HBaseDataStoreService`` controller service can be used to ingest data into an HBase-backed GeoMesa datastore.
For a description of the connection properties, see :ref:`hbase_parameters`.

Accumulo
~~~~~~~~

The ``AccumuloDataStoreService`` controller service can be used to ingest data into an Accumulo-backed GeoMesa
datastore. For a description of the connection properties, see :ref:`accumulo_parameters`.

FileSystem
~~~~~~~~~~

The ``FileSystemDataStoreService`` controller service can be used to ingest data into a file-system-backed
GeoMesa datastore. For a description of the connection properties, see :ref:`fsds_parameters`.

Kafka
~~~~~

The ``KafkaDataStoreService`` controller service can be used to ingest data into a Kafka-backed
GeoMesa datastore. For a description of the connection properties, see :ref:`kafka_parameters`.

Kafka (Confluent)
~~~~~~~~~~~~~~~~~

The ``ConfluentKafkaDataStoreService`` controller service can be used to ingest data into a Kafka topic
associated with a Confluent schema registry. For a description of the connection properties, see :ref:`confluent_kds`.

Redis
~~~~~

The ``RedisDataStoreService`` controller service can be used to ingest data into a Redis-backed
GeoMesa datastore. For a description of the connection properties, see :ref:`redis_parameters`.

PostGIS
~~~~~~~

The ``PostgisDataStoreService`` and ``PartitionedPostgisDataStoreService`` controller services can be used to ingest
data into PostGIS. For a description of the connection properties, see :ref:`pg_partition_parameters`.

GeoTools
~~~~~~~~

The ``GeoToolsDataStoreService`` controller services can be used to ingest data into arbitrary GeoTools data stores.
For a list of stores provided by GeoTools, see the GeoTools
`documentation <https://docs.geotools.org/stable/javadocs/org/geotools/api/data/DataStoreFactorySpi.html>`_.
The data store and its dependencies need to be made available to the controller service through the ``ExtraClasspaths``
property. Once available, the data store should appear in the ``DataStoreName`` property drop-down. Selecting the
data store will display its configuration parameters.
