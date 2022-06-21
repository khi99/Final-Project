{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 연습문제"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Question 1\n",
    "\n",
    "출력 확인"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {
    "ExecuteTime": {
     "end_time": "2021-03-22T22:41:09.896304Z",
     "start_time": "2021-03-22T22:41:09.889304Z"
    }
   },
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "shirt\n"
     ]
    }
   ],
   "source": [
    "a = \"Life is too short, you need python\"\n",
    "\n",
    "if \"wife\" in a: print(\"wife\")\n",
    "elif \"python\" in a and \"you\" not in a: print(\"python\")\n",
    "elif \"shirt\" not in a: print(\"shirt\")\n",
    "elif \"need\" in a: print(\"need\")\n",
    "else: print(\"none\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Question 2\n",
    "- while문을 사용해 1부터 1000까지의 자연수 중 3의 배수의 합을 구해 보자."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "attachments": {
    "image.png": {
     "image/png": "iVBORw0KGgoAAAANSUhEUgAAAGEAAABfCAYAAAD4dql+AAACg0lEQVR4Ae2cQW4CMQxFc/8bcCoWHIQlS6pU/cJEg8eMGmKSVynyKO5kyP95ThipLbfb7U4bq0HBgLEGVP0xIUElwARMGF8KMpRjSIAESAhvzKUUjrEdiQmVI0zoS6xrQhW/bRk2stk+g2uCJgsJA0n43TT+9gOM6GdEiAQRQexjBCZ0PPVEFy0mYEIfvKMrMMvvQQIkQEKlERIgARIgIQEFmIAJlCIdkdmYE9AQMsF7eefl5DTRpx4TspNQV3nbtKrbfojwV7t024qQkJ2E6ppWuKJ1Un2KNsd1nIwQCQgaF/SIVpjwDeXoiLPc8x45kAAJ762YWQmDBEiAhEo3JEACJEBCAgowARMoRTpyhzbm0+n08i91jub0AYjB09FRob37EP9RCVwSqohtk3htvxXcy+l+YtAECWUFVp/i0ZzuJwbKkURWtKKpTzGas7/HdcAERHqUjV5auHtCr4cy7rOxmJDgCxsmYMIzlquWKUiABEio9EMCJEACJCSgABMwgVKkI3loY956QacBeuQ09ioRExKUJNeEusrbptXZ9lsijuY09mrRNUFiWIHVp9gjp7FXibsmSGRFK4z6FP8jZ8dY5XrXhFWEGDlPTMi+MY9cHSs9GxIggW/NlXhIgARIgIQEFGACJlCKdAxnY05AAyZ8iwlbL+iE0qdzeu5MMUTCp4X2njeT+JqLa0IVo226se23wvXI6bkzRtcETdgKrD7FT+f03JnirgkSWdFOXn2KvXN2/Jmud02YabJZ54IJ33JEzbqCZvlckAAJvD+qNEMCJEACJCSgABMwgVKkIzYbcwIaMCGDCdfr9eW/VhMuxL6ls1wul/v5fKYN1KDc+RmuwA9JgRTQHQRhSgAAAABJRU5ErkJggg=="
    }
   },
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Question 3\n",
    "- while문을 사용하여 다음과 같이 별(*)을 표시하는 프로그램을 작성해 보자.\n",
    "![image.png](attachment:image.png)\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Question 4\n",
    "- for문을 사용해 1부터 100까지의 숫자를 출력해 보자."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Question 5\n",
    "- A 학급에 총 10명의 학생이 있다. 이 학생들의 중간고사 점수는 다음과 같다.\n",
    "\n",
    "[70, 60, 55, 75, 95, 90, 80, 80, 85, 100]\n",
    "\n",
    "for문을 사용하여 A 학급의 평균 점수를 구해 보자."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Question 6\n",
    "- 아래 코드는 리스트 중에서 홀수에만 2를 곱하여 저장하는 코드이다.코드를 리스트 내포(list comprehension)를 사용하여 표현하시오."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "numbers = [1, 2, 3, 4, 5]\n",
    "result = []\n",
    "for n in numbers:\n",
    "    if n % 2 == 1:\n",
    "        result.append(n*2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Question 7"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- 주어진 자연수가 홀수인지 짝수인지 판별해 주는 함수(is_odd)를 작성"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Question 8\n",
    "- 람다와 조건부 표현식을 사용하여 코드 작성\n",
    "- 위의 7번을 람다로"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Question 9\n",
    "- 입력으로 들어오는 모든 수의 평균 값을 계산해 주는 함수를 작성하시오."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.7.1"
  },
  "toc": {
   "base_numbering": 1,
   "nav_menu": {},
   "number_sections": true,
   "sideBar": true,
   "skip_h1_title": false,
   "title_cell": "Table of Contents",
   "title_sidebar": "Contents",
   "toc_cell": false,
   "toc_position": {},
   "toc_section_display": true,
   "toc_window_display": true
  },
  "varInspector": {
   "cols": {
    "lenName": 16,
    "lenType": 16,
    "lenVar": 40
   },
   "kernels_config": {
    "python": {
     "delete_cmd_postfix": "",
     "delete_cmd_prefix": "del ",
     "library": "var_list.py",
     "varRefreshCmd": "print(var_dic_list())"
    },
    "r": {
     "delete_cmd_postfix": ") ",
     "delete_cmd_prefix": "rm(",
     "library": "var_list.r",
     "varRefreshCmd": "cat(var_dic_list()) "
    }
   },
   "types_to_exclude": [
    "module",
    "function",
    "builtin_function_or_method",
    "instance",
    "_Feature"
   ],
   "window_display": false
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
