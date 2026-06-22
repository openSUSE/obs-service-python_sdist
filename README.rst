Python setup.py sdist service
=============================

This is an `Open Build Service`_ source service. It creates a source distribution (sdist) from a Python project (containing a setup.py file)

This is the git repository for `openSUSE\:Tools/obs-service-python_sdist`_. The authoritative source is https://github.com/openSUSE/obs-service-python_sdist.

Example
-------
Example _service file:

.. code-block:: xml

    <services>
      <service name="tar_scm" mode="disabled">
        <param name="url">git://github.com/kwwii/horizon.git</param>
        <param name="scm">git</param>
        <param name="package-meta">.git</param>
        <param name="versionformat">1.0.0</param>
        <param name="revision">grizzly-suse-ui</param>
      </service>
      <service name="python_sdist" mode="disabled">
        <param name="basename">horizon-*.tar</param>
      </service>
    </services>

.. _Open Build Service: http://openbuildservice.org/
.. _openSUSE\:Tools/obs-service-python_sdist: https://build.opensuse.org/package/show/openSUSE:Tools/obs-service-python_sdist
