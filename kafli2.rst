Features
========

Extensions
----------

Mathematical symbols
~~~~~~~~~~~~~~~~~~~~

Mathematical symbols are written using a LaTeX syntax and display using
MathJax. Either inline :math:`e^{\cos(x)}` or as equations

.. math::
    \frac{d}{dz} \cos(z) = \sum_{n\in \mathbb N} \frac {d}{dz}\, \frac{(-1)^n}{(2n)!} z^{2n}
    = \sum_{n\geq 1} \frac{(-1)^n}{(2n-1)!}z^{2n-1} = -\sin(z)

Links
~~~~~

It is possible to link to every section, which is useful when making solutions,
in emails and on Piazza.


Geogebra
~~~~~~~~

Geogebra (http://geogebra.org) is an excellent program to make interactive (and good looking)
applets which can be embedded.

.. ggb:: pCuJwqEE
    :width: 700
    :height: 400
    :img: ./03_undirogyfirsumma.png
    :imgwidth: 12cm

|

|

Sage
~~~~

Sage can be used to put in applets written in Sage, Python, Octave, R, etc.
The code can be hidden or shown, which then enables students to play with it.

.. sagecell::

    var ('x y r n'); r = 1; inside = 0; points = []
    n = 100  ## Try changing this! This is the number of shots the estimate is based on
    ### Shoot randomly into the square:
    for i in range(0,n):
        [x,y]=[random(),random()]
        points.append([x,y])
        
    ### If a shot lands inside the circle, make a note of it
        if (y <= sqrt((r^2)-(x^2))):
            inside += 1
        
    ### Approximate pi based on the fraction of shots that landed in the circle
    ### Area of circle = pi*r^2; Area of square = (2*r)^2 = 4*r^2
    ### Shots in circle / Shots in square = (pi*r^2)/(4*r^20 = pi()/4
    piapprox = 4*(inside / n)
    estimate = "Með því að nota "
    estimate += str(n)
    estimate += " punkta, fæst að pi er um það bil "
    estimate += str(piapprox.n())
    show(estimate)
    ### Graph the solution
    circle = []
    for i in range(0,1000):
        x = i/1000
        y = sqrt((r^2)-(i/1000)^2)
        circle.append([x,y])
    graph = list_plot(points)
    graph += list_plot(circle,color='red',figsize=[5,4],plotjoined=true)
    show(graph)


|

|

Panopto
~~~~~~~

Videos from Youtube or Panopto can be embedded.

.. panopto:: f624b32e-178d-41cc-8ccb-a559712471d7
    :width: 720
    :height: 405

|

|

Other
-----

* A <a href="https://edbook.hi.is/stae104g/stae104g.pdf">pdf</a>-version is available who those which to print them out.

* `Index <https://edbook.hi.is/stae104g/genindex.html>`_.

* (Icelandic) translations of mathematical can be shown, 
  for example :hover:`heiltala`.

* Translated word are collected in a `dictionary <https://edbook.hi.is/stae104g/ordaskra.html>`_. 
  This feature uses the dictionary of the Icelandic Mathematical Society (http://stae.is/os).

* It is possible to collect statistics through the web server, Google Analytics and Panopto.
This can be used to see how students use the notes. If there are some parts they use more than others and if there are some parts (e.g. proofs) which they skip.

