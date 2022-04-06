layout: single
title:  "python algorythm ch2"

{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "name": "Untitled1.ipynb",
      "provenance": [],
      "collapsed_sections": []
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "code",
      "source": [
        "# 2.1.7 append로 값 초기화 하기\n",
        "\n",
        "string = \"ABCDEFG\"\n",
        "array = []\n",
        "\n",
        "for i in range(len(string)):\n",
        "  array.append(0)\n",
        "\n",
        "print(array, len(array))"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "9hIacWl4aFup",
        "outputId": "8b3fbf4b-3de2-4f9a-89ce-9e8eab4aee13"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "[0, 0, 0, 0, 0, 0, 0] 7\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# 2.1.7 append로 값 초기화 하기\n",
        "\n",
        "string = \"ABCDEFG\"\n",
        "array = []\n",
        "\n",
        "for i in range(len(string)):\n",
        "  array.append(0)\n",
        "\n",
        "print(array, len(array))\n",
        "print(\"index 0:\", array[0])\n",
        "print(\"index 1:\", array[1])"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "NEBI7F3Uavje",
        "outputId": "9715115d-6456-4706-b068-14cb4d305bf7"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "[0, 0, 0, 0, 0, 0, 0] 7\n",
            "index 0: 0\n",
            "index 1: 0\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# comrehension 방식\n",
        "\n",
        "# array = [0 for i in range(len(string))]\n",
        "\n",
        "# 간단한 방식\n",
        "\n",
        "string = \"ABCDEFG\"\n",
        "array = [0] * len(string)\n",
        "\n",
        "print(array)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "Lw4IHqH_bMm_",
        "outputId": "01b3319b-9950-4580-ee84-5f10ccb97c1f"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "[0, 0, 0, 0, 0, 0, 0]\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "uCsiigcEZycW",
        "outputId": "895bc228-f303-4705-efe8-0bd36e7504c9"
      },
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "None\n"
          ]
        }
      ],
      "source": [
        "# 2.1.8 None이 100개 들어있는 리스트 만들기\n",
        "\n",
        "none_list = [None] * 100\n",
        "#print(none_list)\n",
        "\n",
        "# index 0에 접근하기\n",
        "print(none_list[0])"
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "2.2 리스트 안의 숫자 세기\n",
        "문제 [4,0,4,4,1,8,8,2,2,5,0,5,0]\n",
        "위와 같이 0부터 9사이의 숫자가 들어있는 배열에서 각 숫자가 몇 개씩 들어있는지 출력 "
      ],
      "metadata": {
        "id": "02oJ-bhPdU_U"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# collections 모듈의 counter 사용\n",
        "\n",
        "from collections import Counter\n",
        "num = [4, 0, 4, 4, 1, 8, 8, 2, 2, 5, 0, 6, 5, 6, 0]\n",
        "\n",
        "for k, v in Counter(num).items():\n",
        "  print(k, v)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "51IzmBf4cSvF",
        "outputId": "134ae59d-2859-4c18-82ed-f84426fbef56"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "4 3\n",
            "0 3\n",
            "1 1\n",
            "8 2\n",
            "2 2\n",
            "5 2\n",
            "6 2\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# 정렬\n",
        "num = [4, 0, 4, 4, 1, 8, 8, 2, 2, 5, 0, 6, 5, 6, 0]\n",
        "num = sorted(num)\n",
        "for k, v in Counter(num).items():\n",
        "  print(k, v)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "IoPBHJQReyzx",
        "outputId": "71aadfc5-02eb-47d3-9816-b149c752484f"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "0 3\n",
            "1 1\n",
            "2 2\n",
            "4 3\n",
            "5 2\n",
            "6 2\n",
            "8 2\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# collection 사용x\n",
        "\n",
        "num = [4, 0, 4, 4, 1, 8, 8, 2, 2, 5, 0, 6, 5, 6, 0]\n",
        "memo = [0] * 10 # 0이 10개 있는 memo 리스트 만듦\n",
        "for n in num:\n",
        "  memo[n] += 1\n",
        "\n",
        "for i in range(len(memo)):\n",
        "  print(i, memo[i])"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "zqEGjDGfeyqY",
        "outputId": "734b3299-c92a-4c4c-e012-cce12d87e0b6"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "0 3\n",
            "1 1\n",
            "2 2\n",
            "3 0\n",
            "4 3\n",
            "5 2\n",
            "6 2\n",
            "7 0\n",
            "8 2\n",
            "9 0\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "# 2.3 자리 바꾸기 swap\n",
        "입력한 두 수자의 자리를 바꾼 결과를 출력하는 함수 만들기\n",
        "ex)\n",
        "1, 2 => 2, 1\n",
        "3, 4 => 4, 3\n",
        "4, 5 => 5, 4"
      ],
      "metadata": {
        "id": "3r4_MtlUhqCW"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# 정렬 알고리즘\n",
        "def swap(a, b):\n",
        "  temp = a # 임시 변수 선언하며 a에 있는 값을 보관\n",
        "  a = b # a 값이 들어있던 자리에 b 값으로 덮어쓰기(a값 없어짐)\n",
        "  b = temp # a변수에 있던 값이 b로 덮어쓰기되어 있으므로 대신 저장헤 놓은 temp 값 넣기\n",
        "\n",
        "  print(a, b)\n",
        "\n",
        "swap(1, 2)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "zDQJ4HUSiB1i",
        "outputId": "54bba3cb-30e9-43e3-cf92-fa3b2a8e72fd"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "2 1\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# 배열의 인덱스 값 바꾸기\n",
        "list = [1, 2, 3]\n",
        "print(\"before:\", list)\n",
        "\n",
        "list[0] = list[1]\n",
        "list[1] = list[0]\n",
        "\n",
        "print(\"after:\", list)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "2cJdiH-fie6d",
        "outputId": "81fd69f3-d3ad-412b-91dc-bcbe2c669b6d"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "before: [1, 2, 3]\n",
            "after: [2, 2, 3]\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# 배열의 인덱스 값 바꾸기 temp 추가\n",
        "list = [1, 2, 3]\n",
        "print(\"before:\", list)\n",
        "\n",
        "temp = list[0]\n",
        "list[0] = list[1]\n",
        "list[1] = temp\n",
        "\n",
        "print(\"after:\", list)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "bBGRoabihmZV",
        "outputId": "4b9d1945-4b40-451b-b0a7-8188d6767fb7"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "before: [1, 2, 3]\n",
            "after: [2, 1, 3]\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "# 2.5 중복제거 하기 set\n",
        "입력받은 리스트 L에서 중복을 제거한 리스를 리턴하는 함수를 만들기\n",
        "ex) {1, 2, 2, 3} => {1, 2, 3}"
      ],
      "metadata": {
        "id": "F_pGg5t5kSjr"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# 2.5.1 set: 리스트, 딕셔너리, 튜플과 같이 파이썬의 내장 자료구조 중 하나, 중복 허용x, 셋에 들어있는 값은 고유 값, 중괄호로 정의\n",
        "set_l = {1, 2, 2, 3}\n",
        "print(set_l)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "hdMaoiDikgh3",
        "outputId": "737e1dd1-fd5a-4be2-d64a-294aee3396f8"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "{1, 2, 3}\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# 2.5.2 List를 set으로 바꾸기\n",
        "l1 = {1,2 ,2, 3, 3, 4, 4}\n",
        "s1 = set(l1)\n",
        "\n",
        "print(s1)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "SVB2xUq4lFYU",
        "outputId": "176d07f3-a4ff-45e1-e6ff-260101278aea"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "{1, 2, 3, 4}\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# set을 list로 변환\n",
        "\n",
        "l1 = [1,2, 3, 3, 4, 4]\n",
        "s1 = set(l1)\n",
        "l2 = list(s1)\n",
        "\n",
        "print(l2)"
      ],
      "metadata": {
        "id": "BZfSMzuwlWBo"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "# 2.6 리스트에서 값을 뽑게 될 때\n",
        "while list: 리스트에 값이 있는 동안은 True, 값이 없으면 False가 되기 때문에 리스트가 빌 때까지 값을 뽑음"
      ],
      "metadata": {
        "id": "sLhoQNGEmeCG"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "list = [1, 2, 3, 4]\n",
        "\n",
        "while list:\n",
        "  print(list.pop(0))"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "Po3YfomUmZtv",
        "outputId": "3b43ac33-bd72-4b5c-ba58-b440968221fc"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "1\n",
            "2\n",
            "3\n",
            "4\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# 1~100 까지 출력 "
      ],
      "metadata": {
        "id": "ec2lwXhxy-TN"
      },
      "execution_count": null,
      "outputs": []
    }
  ]
}
