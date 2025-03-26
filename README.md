# PipeAndFilter

<h1>Pipe and Filter Program</h1>
  <p>
        This Java program demonstrates the Pipe and Filter pattern, where a series of processing steps (filters) are applied to an input list.
  </p>

   <h2>Code Explanation</h2>
    <ul>
        <li><b>Input List:</b> A list of integers is provided for processing.</li>
        <li><b>Pipeline of Filters:</b> A list of functions is created, where each function represents a processing step.</li>
        <li>
            <b>Filter Functions:</b>
            <ul>
                <li><b>Filter Even Numbers:</b> Keeps only the even numbers.</li>
                <li><b>Square Numbers:</b> Squares each number.</li>
                <li><b>Filter Numbers Greater Than Ten:</b> Removes numbers that are less than or equal to 10.</li>
                <li><b>New Filter - Filter Numbers Less Than Five:</b> Removes numbers smaller than 5.</li>
            </ul>
        </li>
        <li><b>Pipeline Processing:</b> The input list is processed through the filters sequentially.</li>
        <li><b>Final Output:</b> The filtered and processed list is printed.</li>
    </ul>

   <h2>Details of the New Filter</h2>
    <p>
        <b>Filter Name:</b> filterNumbersLessThanFive<br>
        <b>Functionality:</b> This filter removes all numbers smaller than 5, ensuring only numbers greater than or equal to 5 remain.
    </p>

  <h2>Code Snippet for the New Filter</h2>
    <pre><code>
private static List&lt;Integer&gt; filterNumbersLessThanFive(List&lt;Integer&gt; input) {
    return input.stream()
               .filter(n -&gt; n &gt;= 5)
               .collect(Collectors.toList());
}
</code>
    </pre>
