The three images below are the test overviews for all student, all student name, and highest GPA from Jmeter GUI:

![](/images/Screen Shot 2024-03-13 at 16.18.52.png)

![](/images/Screen Shot 2024-03-13 at 16.32.17.png)

![](/images/Screen Shot 2024-03-13 at 16.36.20.png)

The three images below are the test overviews for all student, all student name, and highest GPA from Jmeter CLI:

![](/images/Screen Shot 2024-03-13 at 18.30.46.png)

![](/images/Screen Shot 2024-03-13 at 18.31.29.png)

![](/images/Screen Shot 2024-03-13 at 18.32.15.png)

These are the original times, before optimization:
![](/images/Screen Shot 2024-03-13 at 20.04.16.png)

![](/images/Screen Shot 2024-03-13 at 20.05.38.png)

![](/images/Screen Shot 2024-03-13 at 20.06.29.png)

These are the times after after optimizing:
![](/images/Screen Shot 2024-03-13 at 20.11.04.png)

![](/images/Screen Shot 2024-03-13 at 20.12.06.png)

![](/images/Screen Shot 2024-03-13 at 20.12.36.png)

1. The difference between JMeter and IntelliJ Profiler:

JMeter only calculates the sample time from when the request is sent until the response is received. Meanwhile, IntelliJ Profiler can also calculate the execution time of each method called.

2. The profiling process can help me identify by examining the flame tree, method list, and timeline, where it will show which part of the code consumes the most time.

3. In my opinion, IntelliJ Profiler is very effective in helping me find the cause of my slow program because it clearly provides CPU Time for each method called.

4. The challenges I face when conducting performance testing and profiling include unfamiliar UI display, inconsistent performance results that do not accurately represent actual speed, and difficulty in finding slow code that can still be improved because methods in libraries that I don't touch are also measured by the profiler. My approach to facing these challenges is by conducting more tests (such as thread groups) and reading more documentation on performance testing and profiling.

5. I can easily find code that can still be optimized quickly. Compared to not using profiling at all, I would have to find the cause of my slow code by reading through all the code one by one, and usually, if found, it only has a slight impact on performance.

6. I handle situations where the profiling results are inconsistent by conducting more testing such as thread groups or avoiding initial measurements when the program is running because the JIT compiler on the JVM is not fully optimized yet, making it slower.

7. The strategy to optimize code is to create a database containing a lot of data, then profile the existing endpoints. This way, the time difference will be clearly visible if there are parts of the code that need optimization. Examples of code that can be improved include replacing recursion with iteration such as for/while loops and replacing strings with StringBuilder to improve performance. To ensure that my changes do not disrupt the functionality of the application, unit tests and functional tests need to be rerun.
