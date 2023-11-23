{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "authorship_tag": "ABX9TyMh2hNE+XQkD7Gtwpn/v9Im",
      "include_colab_link": true
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
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/erShwetaMondal/CodeCamp/blob/main/Basic_Coding.ipynb\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "input_value = input(\"Enter a number: \")\n",
        "\n",
        "if input_value.isdigit():\n",
        "    input_value = int(input_value)\n",
        "    if input_value == 17:\n",
        "        output_value = \"b36\"\n",
        "    else:\n",
        "        output_value = f\"b{input_value + 19}\"  # General pattern starting from 20\n",
        "\n",
        "    print(f\"Output: {output_value}\")\n",
        "else:\n",
        "    print(\"Invalid input. Please enter a number.\")"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "z6H4z1Z4hBc9",
        "outputId": "7cba16dd-8d11-4ea7-c5e1-ddd71d83e9a8"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Enter a number: 17\n",
            "Output: b36\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "x = 2\n",
        "y = 2\n",
        "total_value = x + (2 * y)\n",
        "\n",
        "if total_value % 2 == 0:\n",
        "    print(\"YES\")\n",
        "else:\n",
        "    print(\"NO\")\n"
      ],
      "metadata": {
        "id": "ZDKpDoqh-UX0",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "5164cd52-2478-4bcd-a090-3c070539b88a"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "YES\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "def is_magic_number(num):\n",
        "    while num > 9:\n",
        "        sum_of_digits = 0\n",
        "        while num > 0:\n",
        "            sum_of_digits += num % 10\n",
        "            num //= 10  # Update num by removing the last digit\n",
        "        num = sum_of_digits  # Update num to the sum of its digits\n",
        "\n",
        "    if num == 9:\n",
        "        return True\n",
        "    else:\n",
        "        return False\n",
        "\n",
        "number_to_check = 199  # This assignment should be outside the function\n",
        "\n",
        "if is_magic_number(number_to_check):\n",
        "    print(f\"{number_to_check} is a magic number!\")\n",
        "else:\n",
        "    print(f\"{number_to_check} is not a magic number.\")"
      ],
      "metadata": {
        "id": "ODB5FmXpBLQo",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "50fd0f81-0fa3-449b-ec95-94a3cee06037"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "199 is not a magic number.\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "def groupAnagrams(strs):\n",
        "    anagram_dict = {}\n",
        "    for word in strs:\n",
        "        sorted_word = ''.join(sorted(word))\n",
        "        if sorted_word in anagram_dict:\n",
        "            anagram_dict[sorted_word].append(word)\n",
        "        else:\n",
        "            anagram_dict[sorted_word] = [word]\n",
        "    return list(anagram_dict.values())\n",
        "\n",
        "# Example usage\n",
        "strs = [\"eat\", \"tea\", \"tan\", \"nat\", \"bat\"]\n",
        "output = groupAnagrams(strs)\n",
        "print(output)"
      ],
      "metadata": {
        "id": "juzuwQQHDswv",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "377718a3-7d64-4997-fb23-a6a22d0a3dc6"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "[['eat', 'tea'], ['tan', 'nat'], ['bat']]\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "def maxprofit(prices):\n",
        "    max_profit = 0\n",
        "    for i in range(1, len(prices)):\n",
        "        if prices[i] > prices[i - 1]:\n",
        "            max_profit += prices[i] - prices[i - 1]\n",
        "    return max_profit\n",
        "prices = [1, 2, 3, 4, 5]\n",
        "profit = maxprofit(prices)\n",
        "print(\"Maximum profit:\", profit)"
      ],
      "metadata": {
        "id": "XQbk462iHs2r",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "434ff5ed-53b6-4948-c8a0-49cc8690cdae"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Maximum profit: 4\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "a = list(range(1, 11))\n",
        "search_num = int(input(\"Enter a number: \"))\n",
        "if search_num in a:\n",
        "    print(\"True\")\n",
        "else:\n",
        "    print(\"False\")"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "xiOULGZImlvc",
        "outputId": "deaa9a9f-1ea0-4c85-8a46-367c14c88de3"
      },
      "execution_count": 52,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Enter a number: 7\n",
            "True\n"
          ]
        }
      ]
    }
  ]
}
