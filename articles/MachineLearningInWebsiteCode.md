
<!--
.. title: Machine learning in website code
.. slug: MachineLearningInWebsiteCode
.. date: 2018-10-04 19:10:28 UTC+01:00
.. tags:
.. category:
.. link:
.. description:
.. type: text
-->


## The problem

If you try to use TensorFlow in a website's code on PythonAnywhere, it probably
won't work.   This is because it tries to create new threads (in a slightly odd
way), and then crashes.  The crash is so serious that you probably won't even
see anything in the error log -- just a message in the server log saying that
your worker processes died.

## The solution

Unfortunately we don't have a good solution for this if you're using TensorFlow
directly :-(

However, if you're using Keras with a TensorFlow backend, you can work around
the issue -- just switch to using the Theano backend instead.   That has been
confirmed to work.
