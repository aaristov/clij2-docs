## countTouchingNeighbors
<img src="images/mini_empty_logo.png"/><img src="images/mini_clij2_logo.png"/><img src="images/mini_clijx_logo.png"/><img src="images/mini_empty_logo.png"/>

Takes a touch matrix as input and delivers a vector with number of touching neighbors per label as a vector.

Category: [Measurements](https://clij.github.io/clij2-docs/reference__measurement)

### countTouchingNeighbors often follows after
* <a href="reference_generateTouchMatrix">generateTouchMatrix</a> (1)


### countTouchingNeighbors is often followed by
* <a href="reference_release">release</a> (5)
* <a href="reference_paste2D">paste2D</a> (1)


### Usage in ImageJ macro
```
Ext.CLIJ2_countTouchingNeighbors(Image touch_matrix, Image touching_neighbors_count_destination);
```


### Usage in object oriented programming languages



<details>

<summary>
Java
</summary>
<pre class="highlight">// init CLIJ and GPU
import net.haesleinhuepf.clij2.CLIJ2;
import net.haesleinhuepf.clij.clearcl.ClearCLBuffer;
CLIJ2 clij2 = CLIJ2.getInstance();

// get input parameters
ClearCLBuffer touch_matrix = clij2.push(touch_matrixImagePlus);
touching_neighbors_count_destination = clij2.create(touch_matrix);
</pre>

<pre class="highlight">
// Execute operation on GPU
clij2.countTouchingNeighbors(touch_matrix, touching_neighbors_count_destination);
</pre>

<pre class="highlight">
// show result
touching_neighbors_count_destinationImagePlus = clij2.pull(touching_neighbors_count_destination);
touching_neighbors_count_destinationImagePlus.show();

// cleanup memory on GPU
clij2.release(touch_matrix);
clij2.release(touching_neighbors_count_destination);
</pre>

</details>



<details>

<summary>
Matlab
</summary>
<pre class="highlight">% init CLIJ and GPU
clij2 = init_clatlab();

% get input parameters
touch_matrix = clij2.pushMat(touch_matrix_matrix);
touching_neighbors_count_destination = clij2.create(touch_matrix);
</pre>

<pre class="highlight">
% Execute operation on GPU
clij2.countTouchingNeighbors(touch_matrix, touching_neighbors_count_destination);
</pre>

<pre class="highlight">
% show result
touching_neighbors_count_destination = clij2.pullMat(touching_neighbors_count_destination)

% cleanup memory on GPU
clij2.release(touch_matrix);
clij2.release(touching_neighbors_count_destination);
</pre>

</details>



<details>

<summary>
Icy JavaScript
</summary>
<pre class="highlight">// init CLIJ and GPU
importClass(net.haesleinhuepf.clicy.CLICY);
importClass(Packages.icy.main.Icy);

clij2 = CLICY.getInstance();

// get input parameters
touch_matrix_sequence = getSequence();
touch_matrix = clij2.pushSequence(touch_matrix_sequence);
touching_neighbors_count_destination = clij2.create(touch_matrix);
</pre>

<pre class="highlight">
// Execute operation on GPU
clij2.countTouchingNeighbors(touch_matrix, touching_neighbors_count_destination);
</pre>

<pre class="highlight">
// show result
touching_neighbors_count_destination_sequence = clij2.pullSequence(touching_neighbors_count_destination)
Icy.addSequence(touching_neighbors_count_destination_sequence);
// cleanup memory on GPU
clij2.release(touch_matrix);
clij2.release(touching_neighbors_count_destination);
</pre>

</details>





### Example notebooks
<a href="https://clij.github.io/clij2-docs/md/spots_pointlists_matrices_tables"><img src="images/language_macro.png" height="20"/></a> [spots_pointlists_matrices_tables](https://clij.github.io/clij2-docs/md/spots_pointlists_matrices_tables)  




### Example scripts
<a href="https://github.com/clij/clij2-docs/blob/master/src/main/macro/division_visualisation.ijm"><img src="images/language_macro.png" height="20"/></a> [division_visualisation.ijm](https://github.com/clij/clij2-docs/blob/master/src/main/macro/division_visualisation.ijm)  
<a href="https://github.com/clij/clij2-docs/blob/master/src/main/macro/spots_pointlists_matrices_tables.ijm"><img src="images/language_macro.png" height="20"/></a> [spots_pointlists_matrices_tables.ijm](https://github.com/clij/clij2-docs/blob/master/src/main/macro/spots_pointlists_matrices_tables.ijm)  


[Back to CLIJ2 reference](https://clij.github.io/clij2-docs/reference)
[Back to CLIJ2 documentation](https://clij.github.io/clij2-docs)

[Imprint](https://clij.github.io/imprint)
