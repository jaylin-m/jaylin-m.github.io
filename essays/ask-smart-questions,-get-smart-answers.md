---
layout: essay
type: essay
title: "Ask Smart Questions, Get Smart Answers"
# All dates must be YYYY-MM-DD format!
date: 2025-01-30
published: true
labels:
  - Software Engineering
  - StackOverflow
  - Questions
  - Answers
---

<img width="700px" class="img-fluid" src="../img/ask-smart-questions,-get-smart-answers/questions.png">

## The Importance of Asking Smart Questions for Software Engineers

Asking smart questions is a critical skill for software engineers because it allows them to efficiently seek help from forums, email lists, newsgroups, or chat boards to resolve issues. A smart question demonstrates the querent’s effort to research the problem beforehand, such as searching relevant resources, attempting possible solutions, and providing a clear explanation of the issue. This not only saves time for both the querent and the respondent but also encourages knowledgeable experts to engage and take the time out of their busy day to help, since they can quickly understand the problem and see that the querent has made an effort to solve it. By presenting a well-prepared, thoughtful question that includes background information and a clear goal, a software engineer increases their chances of receiving helpful, relevant responses. Asking smart questions fosters effective communication and problem-solving, benefiting both the querent and the larger development community.

## Example of a Smart Question

<img width="700px" class="img-fluid" src="../img/ask-smart-questions,-get-smart-answers/stackoverflow.png">

This querent, who titled their question <a href="https://stackoverflow.com/questions/79375931/storing-and-retrieving-number-from-c23-experimental-simd-gives-random-result">*Storing and retrieving number from C++23 experimental simd gives random result*</a>, is encountering unpredictable behavior in their C++ code. Identical printf functions print different numbers, with the values varying each time the app is run — sometimes positive, sometimes negative. When they use vfloat4 instead of vint4, all the printed numbers are zero. The querent is unsure where to begin debugging.

This is an example of a smart question because, first, it uses a meaningful and specific subject header. Second, it's written in clear, grammatical, and correctly spelled language. Third, it describes the symptoms of the bug carefully and clearly, as well as the environment in which it occurs, including the compiler, OS, and CPU. Fourth, it describes the diagnostic steps the querent took to try to resolve the issue themselves before asking the question. Fifth, the querent uses appropriate tags in their post that align with the topic of their question. Lastly, the user also provides a minimal, bug-demonstrating test case that illustrates the problem, offering just enough code to show the undesirable behavior without including unnecessary lines or excessive details.

The querent provides a minimal amount of code to test the problem:

```
#include <experimental/simd>

namespace stdx = std::experimental;

using vfloat4 = stdx::fixed_size_simd<float, 4>;
using vint4 = stdx::fixed_size_simd<int, 4>;

inline void print_vint4(vint4 vi4)
{
    printf("%i %i %i %i\n", vi4[0], vi4[1], vi4[2], vi4[3]);
}

int main()
{
    vint4 _v = 4;
    printf(">> %i\n", _v[0]);
    printf(">> %i\n", _v[0]);
    print_vint4(_v);
    return 1;
}
```

## Example of a Not Smart Question

This querent, who titled their question <a href="https://stackoverflow.com/questions/79400124/using-useeffect-keep-on-calling-api">*using useEffect keep on calling api*</a>, is trying to call a REST API using useEffect, but the API keeps being called continuously.

This is an example of a not smart question because, first, the subject header is not meaningful or specific — it’s vague and lacks context. Second, it's not written in clear, grammatical, and correctly spelled language. Third, it does not describe the environment in which it occurs. Fourth, it does not describe the diagnostic steps the querent took to try to resolve the issue themselves before asking a question. Lastly, the user does not provide a sufficient bug-demonstrating test case that illustrates the problem. They only mention that 'user' is from createContext, but do not provide any further context or explanation.

A portion of the code the querent provided:

```
  useEffect(() => {
    const fetchData = async () => {
      try {
        const recievedUser = await Apis.getUser(user);
        setProfile(recievedUser.data);
        if (recievedUser.data) {
          // console.log(imageUrl)
          fetchImage();
        }
      } catch (error) {
        console.log(error.response);
      }
    };
```

## Asking Smart Questions: A Path to Clear and Effective Solutions

I gained insight into what it means to ask a smart question. A smart question reflects that the person asking has already attempted to find an answer using various resources, such as searching the archives of relevant forums or mailing lists, browsing the web, or reading manuals and FAQs. It also involves posting the question in an appropriate, on-topic forum. Asking a smart question requires using a meaningful, specific subject header that immediately conveys the issue at hand, allowing the respondent to understand the problem at a glance. Writing clearly, with correct grammar and spelling, is essential, so is being precise and informative about the problem. When describing the issue, it's important to explain the symptoms of the problem or bug in detail, including the environment in which it occurs, such as the machine, OS, or application. The questioner should also describe the research they conducted before asking, to demonstrate that they made an effort to find the answer independently. They should also describe the diagnostic steps they took to troubleshoot the issue, and any recent changes to their system or software configuration. The problem should be described in chronological order, and the focus should be on describing the desired goal rather than the specific steps taken to reach it. Following these guidelines ensures that you ask a smart question, which in turn increases the likelihood of receiving smart, helpful answers.
