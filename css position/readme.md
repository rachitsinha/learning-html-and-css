position: static;
    this is the default position property of elements when they are first rendered, in the sequence they appear in the HTML document.


position: relative;
    this has the same effect as "static", but additionally allows to apply (left, right, top, bottom) positioning properties to the element. 
    E.g. {
        position: relative;
        top: 10px;
        left: 15px;
    } 
    This will positon the element 10px top and 25px left of what it would have naturally been (i.e. relative to itself).


position: absolute;
    this removes the element from the naturally occuring document flow and positions it relative to:
        a) the html page
        OR
        b) the first ancestor in hierarchy which has 
                { position: relative; } 
            property applied.
    E.g. {
        position: absolute;
        top: 10px;
        left: 15px;
    }
    This will position the element 10px from top and 15px left of either the HTML page, or the first ancestor in hierarchy which has { position: relative; } property applied. This also allows scrolling of other elements around it, keep this element fixed in this position.


position: fixed;
    this has the same effect as { position: absolute; }, but it always positions relative to the HTML page. It does not consider the closest ancestor with { position: relative; }.

    E.g. {
        position: fixed;
        top: 10px;
        left: 15px;
    }
    This will position the element 10px from top and 15px from left of html page and keep it fixed there, even if page is scrolled.


position: sticky;
    The element will scroll along with its container, until it is at the top of the container (or reaches the offset specified in top), and will then stop scrolling, so it stays visible.
