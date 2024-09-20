This is a report to showcase my final report during Google Summer of Code 2024 with SymPy project. SymPy is a library that provides API for symbolic mathematics and physics computations.

The SymPy community has been very welcoming and supportive for me. I started contributing in SymPy and later developed interest for the control package. I applied for GSoC 2024 and got selected in SymPy for the the project `Improving and Expanding the Functionalities of the Control Module.`
## About Me
I'm [Abhishek Kumar](https://github.com/abhiphile) a final-year undergraduate student pursuing a major in Electronics and Communication Engineering from National Institute of Technology (NIT) Delhi. I'm interested in physics, algorithms and computer science. I like to contribute on open source repositories and collaborate on interesting projects.
# Project: Improving and Expanding the Functionalities of the Control Module \
Student: Abhishek Kumar [abhiphile](https://github.com/abhiphile) \
Mentor: Nikhil Maan [Sc0rpi0n101](https://github.com/Sc0rpi0n101) \
Project Length: 350 Hours \
Proposal Link: [Improving and Expanding the Functionalities of the Control Module](https://docs.google.com/document/d/1dmm7goYEyVcVkXrpwJm84yp6BmwfKrLB9rntZDA7R8g)
## Project Summary
In this project, I focused on enhancing the `Series`, `MIMOSeries`, `Parallel`, `MIMOParallel`, `Feedback`, and `MIMOFeedback` classes to support `StateSpace` interconnections. I worked on solving the state space equations using `dsolve()`. Additionally, I introduced a new `PIDController` class which can be used for various regulatory applications. I also incorporated mechanics and electrical textbook problems that can be addressed using `StateSpace`. Finally, I implemented new plotting features, including the Nyquist plot (`nyquist_plot`) and Nichols plot (`Nichols Plot`), utilizing SymPy's own `plot_parametric` function.
## Related Work
Here’s a summary of my work on SymPy as part of Google Summer of Code (GSoC 24):
### Merged Pull Requests
1. ( [#26647](https://github.com/sympy/sympy/pull/26647) ) In this PR I've worked on refactoring the `Series` and `MIMOSeries` classes to support `StateSpace` interconnections. Previously these connections were only possible with `TransferFunctions`, `doit()` for `StateSpace` interconnections behave differently, for these interconnections `doit()` will return the resulting `StateSpace` object.
2. ( [#26718](https://github.com/sympy/sympy/pull/26718) ) In this I've # Added support of using `StateSpace` with `Parallel` and `MIMOParallel`. It is similar to the PR described above.
3. ( [#26863](https://github.com/sympy/sympy/pull/26863) ) This PR was related to make `Feedback` and `MIMOFeedback` compatible with `StateSpace`.
4. ( [#26685](https://github.com/sympy/sympy/pull/26685) ) & ( [26736](https://github.com/sympy/sympy/pull/26736) ) Implemented a method to find out the output vector using the `dsolve` function in `StateSpace` object. The first PR was related to adding functions like `state_vector` and `output_vector`. In the second PR I've removed the `state_vector` method and renamed the `output_vector` to `dsolve`. This was suggested by Jason K. Moore because it matches with existing functionality of SymPy.
5. ( [#26768](https://github.com/sympy/sympy/pull/26758) ) Added test to check the functionality of `StateSpace` using symbolic matrices.
6. ( [#26781](https://github.com/sympy/sympy/pull/26781) )`PIDController` class has been added to control. This class can be useful for various control applications which require regulation. Since it's parent class is `TransferFunction` it supports all the functionality of `TransferFunctions`.
7. ( [#26978](https://github.com/sympy/sympy/pull/26978) ) This PR add two problems related to state space in `electrical_problems.rst` file. These examples can help users to understand how SymPy's control module can be helpful in solving problems related to physics using `StateSpace` and `Sympy`.
8. ( [#270009](https://github.com/sympy/sympy/pull/27009) ) Added a simple spring mass damper problem and a rotational system problem to control tutorials.
### Open Pull Requests:
1. ( [#27052](https://github.com/sympy/sympy/pull/27052) ) Implemented Nyquist Plot, this plot uses SymPy's own `plot_parametric` method to plot the output.
2. ( [#27067](https://github.com/sympy/sympy/pull/27067) ) Added Nichols plot to control plots.
3. ( [#26836](https://github.com/sympy/sympy/pull/26836) ) Added a method to calculate bandwidth of a `TransferFunction`.

## Future Work
* Adding a Discrete time model that includes **Discrete TransferFunction** and **Discrete StateSpace** model.
## Acknowledgements
I am highly grateful to my mentor, [Nikhil Maan](https://github.com/Sc0rpi0n101) for always being there with me whenever I was struck and needed help. I would also like to thank [Anurag Bhat](https://github.com/faze-geek) for reviewing my PR. I would like to thank Jason Moore ([@moorepants](https://github.com/moorepants)), Oscar Benjamin([@oscarbenjamin](https://github.com/oscarbenjamin)), Christopher Smith([@smichr](https://github.com/smichr)), Aaron Meurer([@asmeurer](https://github.com/asmeurer)), S.Y. Lee ([@sylee957](https://github.com/sylee957)), and other members and contributors in the community for their continuous support, allowing me to contribute to Sympy and learn a lot in the process.
## References
1. My GSoC Proposal: [Proposal](https://docs.google.com/document/d/1dmm7goYEyVcVkXrpwJm84yp6BmwfKrLB9rntZDA7R8g)
2. Mathworks control system documentation: [MATLAB Control Documentation](https://in.mathworks.com/help/control/ref/tf.html)
3. python-control documentation: [python-control](https://python-control.readthedocs.io/en/latest/generated/control.TransferFunction.html)
4. The SymPy Github page is for issues/ pull requests/ comments.
5. [Book on Control by Karl J. Åström and Richard M. Murray](https://docs.sympy.org/latest/modules/physics/control/lti.html#module-sympy.physics.control.lti)
