.. _-respondWithSingletonHeaders-:

respondWithSingletonHeaders
===========================

Adds the given HTTP headers to all responses coming back from its inner route only if a respective header with the same
name doesn't exist yet in the response.


Signature
---------

.. includecode:: /../spray-routing/src/main/scala/spray/routing/directives/RespondWithDirectives.scala
   :snippet: respondWithSingletonHeaders


Description
-----------

This directive transforms ``HttpResponse`` and ``ChunkedResponseStart`` messages coming back from its inner route by
potentially adding the given ``HttpHeader`` instances to the headers list.
A header is only added if there is no header instance with the same name (case insensitively) already present in the
response. If you'd like to add only a single header you can use the :ref:`-respondWithSingletonHeader-` directive instead.


Example
-------

See the :ref:`-respondWithSingletonHeader-` directive for an example with only one header.