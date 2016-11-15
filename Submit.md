HELLO.

THIS IS THE PROJECT FOR PROJECT7 UDACITY

Experiment Overview: Free Trial Screener

At the time of this experiment,
Udacity courses currently have two options on the home page: "start free trial", and "access course materials".

If the student clicks "start free trial", they will be asked to enter their credit card information, and then they will be enrolled in a free trial for the paid version of the course. After 14 days, they will automatically be charged unless they cancel first.

If the student clicks "access course materials", they will be able to view the videos and take the quizzes for free, but they will not receive coaching support or a verified certificate, and they will not submit their final project for feedback.


In the experiment, Udacity tested a change where if the student clicked "start free trial", they were asked how much time they had available to devote to the course.

If the student indicated 5 or more hours per week, they would be taken through the checkout process as usual.

If they indicated fewer than 5 hours per week, a message would appear indicating that Udacity courses usually require a greater time commitment for successful completion, and suggesting that the student might like to access the course materials for free. At this point, the student would have the option to continue enrolling in the free trial, or access the course materials for free instead. This screenshot shows what the experiment looks like.


The hypothesis was that this might set clearer expectations for students upfront, thus reducing the number of frustrated students who left the free trial because they didn't have enough time—without significantly reducing the number of students to continue past the free trial and eventually complete the course.

If this hypothesis held true, Udacity could improve the overall student experience and improve coaches' capacity to support students who are likely to complete the course.

The unit of diversion is a cookie, although if the student enrolls in the free trial, they are tracked by user-id from that point forward. The same user-id cannot enroll in the free trial twice. For users that do not enroll, their user-id is not tracked in the experiment, even if they were signed in when they visited the course overview page.


Metric Choice

Which of the following metrics would you choose to measure for this experiment and why? For each metric you choose, indicate whether you would use it as an invariant metric or an evaluation metric. The practical significance boundary for each metric, that is, the difference that would have to be observed before that was a meaningful change for the business, is given in parentheses. All practical significance boundaries are given as absolute changes.

Invariant metric :
Number of cookies,
Number of clicks on "Start free trial",
Click-through-probability on "Start free trial"

Invariant metric is the metric not affected by the change during the experiment
In the explanation, we are going to notify students who are enrolling the class that they need to spend significant time for the class. It means the notification message will trigger after clicking enrolling the class. So, Number of cookies, which is number of unique cookies to view the course overview page would not be affected. Also, Number of clicks, which is a number of unique cookies clicking the "Start free trial" not affected by the notification. Same as the click through probability. It is the process before the notification message. So, they would be a good metrics for invariant metrics.

Variant metric :
Gross conversion,
Net conversion


Any place "unique cookies" are mentioned, the uniqueness is determined by day. (That is, the same cookie visiting on different days would be counted twice.)
User-ids are automatically unique since the site does not allow the same user-id to enroll twice.
Number of cookies: That is, number of unique cookies to view the course overview page. (dmin=3000)
Number of user-ids: That is, number of users who enroll in the free trial. (dmin=50)
Number of clicks: That is, number of unique cookies to click the "Start free trial" button (which happens before the free trial screener is trigger). (dmin=240)
Click-through-probability: That is, number of unique cookies to click the "Start free trial" button divided by number of unique cookies to view the course overview page. (dmin=0.01)
Gross conversion: That is, number of user-ids to complete checkout and enroll in the free trial divided by number of unique cookies to click the "Start free trial" button. (dmin= 0.01)
Retention: That is, number of user-ids to remain enrolled past the 14-day boundary (and thus make at least one payment) divided by number of user-ids to complete checkout. (dmin=0.01)
Net conversion: That is, number of user-ids to remain enrolled past the 14-day boundary (and thus make at least one payment) divided by the number of unique cookies to click the "Start free trial" button. (dmin= 0.0075)


You should also decide now what results you will be looking for in order to launch the experiment. Would a change in any one of your evaluation metrics be sufficient? Would you want to see multiple metrics all move or not move at the same time in order to launch? This decision will inform your choices while designing the experiment.
the notification message would affect the students who enrolled class even after the free trial days. students who are not confident devote themselves more than 5 hours would not take the classes which made students who enrolled the class would survive more than before even though the number of students who enrolled the class might decrease but the probability, the number of students made first payment divided by the number of students who started first trial, would be increased.

So, we will calculate probability for gross conversion and net conversion. It could show how the survivors rate increased.
