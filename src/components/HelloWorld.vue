<template>
  <div class="page-container">
    <md-app md-mode="reveal">
      <md-app-toolbar style="background-color: black;" >

        <div class="sp">
          <md-icon class="bt-primary" ></md-icon>
        <img style="height: 15%; width: 15%; margin-right: 10px;" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAVMAAACVCAMAAADSU+lbAAABHVBMVEUAAAD////pVSLuVyMSEhIVFRXgUiFmJg+qPhmgoKArKyuKNBYFBQWxsbGysa+5ubmaOBdHRkXc3NtVUk6jOxgfHRuZmZmvQBkbGxtJGwusrKyOjYz09PQjIyOmpqY7Ozve3t4yMjJjY2PKysrv7+/BwcF3d3eAgIBYWFhfX19OTk6Kiopubm7m5uYoKCjR0dE2EwjKSh3YTyCBOiI+Fwm/Rhx6LhQxEgiFMROTNhVKSUYUCwcjEgszLyz2WyTTVittKhNWHw0rDwYkIxwtLSB6LBEZCAI5ODBrLRgdFxN7d2+vrqS+TygaGwcyLTcvFg2yVjdFHw3wbDleXlScRSdGRjzkYjZuOiiIRCwnFhE8HRHxUhqbTDCzTCsvODnRK3MEAAAfJUlEQVR4nO1dCXvbRpJtiKBkIKBgQBIEA437vohIsRxLsmTJORxnPZvNZGZ2Z7Kz//9nbHWDOAlSVJxEzBe+zxalJtBovK6uqj6qG6Eddthhhz8I3r28P7j7guDu/sXn109dnD82gMy718cX53uTFvtnp5evDl58uaP28fj2/vXz0zNK414PFbMXx58dvHvqMv6xcPCMSufeSlQSe/ftUxf0D4Lrb07P99fx2fK6t3/6eqcEHsKbg+O92w347Mjrs4M3T13qrcari7UtfgWrp99shbAKI2ns2K9woQAYJDX/p/X15BLEWqsyHHveEu6A0ccRuqB17+zVJvn/1vheVpJQ4btJ14dl9UsRkZ9TVyUfupwgdFVk5He1Svrephcg1w5RJEvwmxOk8EPPrVgnfyIjOSEfikw/UDDbgNP7yQpGO7Z/xA9YsHr+xdPL6pVvAF9+0k1zcU4+IuYr8hHjlHzkOIaf/g35/Qgf0SSffoNSH74SbchIyOeIlwnTEc0iZ8hN6AYr9IPJHizP/cXtOJ3752cXF6fPnl8Cnj87vTg7IxZsidjJ5OK7X4OXT4FEOEWZrQo3J+G8Sks5G36e5MzX8DH9SQtIols0nLLJYZUkX9Hrr+wYqbnmfUBCzKOAo4kn1RX0jxvdA7E9OfKUh4pzeT7C0u3exfHlNy++7HlM335+/+ry+GJ/MjRlk73LLz+dl0+B5BMiLZxP5SNtoQajuaYjQbrxCaeWixiSCML74eSGcurECJP3c+VKTq+A7nmkmjNImiP8ntyVpkCqdSTJ5AbrJNBB4PlDbX1hPj9d9uxvz56/uv98xQ3XXwKxZ0usvn1aUa04dXCG8Ic6LTPCcm7kiHL6/Q3SbfhMcHQUx5hQFDpIKVCHU5BTQ+eR9h8onn+FiXJmPSAY6QIqiaBa0nt8DZUjm2vL8s1QkYJ6fL6Kzg6+fLbfv3My+fiUvYCK0ytfQrhJiyTk6X9/Tzk94eKr0L7qtv0TM7nKi6uW0xS+MjIe/cVTjk4Q8z1JC0B1vtekK50IuXWFAv1IQuU6Tq8vb4eMXnyx4Vu8ubzoS/jk7f0vouNXgeUTE04UXctpLqG8ALp8sFEJoZzTGk5B+yZGnURtvQWcpsgIIfU/C9CzZkF8pwByvCI6NQAebyR0wkCCt4bTN8/7QgpO/N0jTPi7131WJ+eb1sevj5AJb1wtn6KvGBelMk3TwGYrJ2CmI6RTtypicpTBf2RBUkSTyJ8RYya5F4J1D5ElEmV8ZQKfUeBeH3ku0g+J16ozCVKASwWqhPFWluOHj0NG7x/ZfN/dn3cV62Tvv34ZI58M1QFzQs29I/CCQI31nHeIpLEO4tX5HLQjfMNP4UIBkhyDnxtNkiNJDrnQEgy+4+dLIOmI5XloAuwcOSrPE9EGiTaMFeX48m2/6X78caywvBRDWa/cOE4lnl2+4NX+pFMrT9j6twGfn/fb7fOlK5xc58SSgXZiyQwAl4ecXvUoOnhxWuvkyT+e3E19Wvx40aP041DCTqKg9AmTjGyBMmnge0E4uPSyEtXJX//klL4761r8288G40t64eOaRHA7TKYLXCw6yDVekMwme2O640+E6/MOpZP9g+53QnrYIVCGjhrpBhdMH9XgQo1nt5PJi9/3FbYOz7qUnvfafTzDLXO+gubA8CHIpVb2SfXN7kjYx/273/cNtg6X3XZ/1hUwR+sIZJHFKKfmiSlnN9OQ67Pa7aK9G+jjl8fHzzfB6ULpHJxucvWzz35zan4pXnUpPe2q0rAjo0U+7yZg20V8X7EyRbLqEQf7exvhdtEPvtxo9HZytuJxg3L1gb2rx3PkDpVdD/nw8pcdL2py0ZkCtYKWreA9+LwJknpZ61co83qZ6yu839+Z00ELGsLbaFy+ixyvyw8PXR902irTycXLNj2p+bNFHbzQ2Cygc+v6vdyOkNt/WjAuA9vF6TIHD+BafFx+dy2lt//4oU2PKrICPSc0KSVl2ER5R1L9KA8+xP38C3f7OWW8VZ3JFcgfyG8w0P+yfdvJ/r86X/Bx6ObWnDaTRmQZDf3U/F5chz5jx8LgAWOkbpM+JYhW3LgC5drMfH/AaceNmtyNZOeEingStRm0zV9eFD0TBo8caVkNp5P1aDi97SW3RexjFadhIFbQDoNRTVg8itJoNAtRMzWNUxQ9d/sTqvedMY+/NQN7gp4jI3dZIaRu6E9uJy8FfU9I9SM0W6ToUr+t+cuk1pyeH6/Hs4WJPHjWTX1+Vhfx7Hnv8lW+FKtOKViEjFgZY+SB6Y4ePvgjGRxejYwgVeQ9ayidvG29KJ3hEHRHpYUBUt7LPVJBpxbWvPUKPEnvPQ8v+VQLTifPHih+W6u95KaUv8ghvRmhxLcevq+GN3L/mqnSFx291fr6LhMg0Jry+0UFlSjo5qegOOx7F37UJR3w1eA5m3K6Ap/GKXKZZQSb3z0ipuvuPm44vW2Lm2IbkQaj1BWMm2Ze4Xq5mAOt5U/7z3laTp0RG+Ov7J8MYATLN6+zcd+25ni/mcl7XzJHMdSN72oNp11DSqez3bVOMDhdfVKfltOTMfdS3NDxH/Oj6CTWCrweE1Od0VXCWIBqoccnbZ9Udg2U2yka1fwd9LtrT8zpmKiN+nwjGBMeWVp9/VmzUudt04GSGBHRelWSOjscL/qk2D6CLitRtQI6HHlWtyp7i5W2g1NcdgmSN7p3VHbWcNrx99upkgAnVFkWHcOkI5ukBCB8btWOFGStd4QZrvuk7eDUlnpl1je4VaprQe5aqjWctmN8+43RdxndoLeLnd6DiGTG50CJRCJuCiSt55RRO0/aDk4L6ahbQPvDw7fWmhgfdatjNafXp3VRb9t3LZmFQbpJ2popUcSBQ2fJbdvxXfT9ek67/sZ2cAq2vudrPuz4N3YkmvbUxkpOXzbq9LYR05xx00p3omxRQ35RDThKfU1fOqjv6Q9RdB68HXa/SNq2TP9OH7iRL5t3MbqvtprTthO+XyepAV5wqZDBncILxKgyNtLh0AAGaD5qTxtwS496Yk5taTBk9ZCg1h19HCF+M06/aaz+xzrJOMwWBj1BrqnH1ey9JIZohL5DZK31Ur3W9G8Hp7KDFmsTajjrb2w4FDbltFkeNWnXi6ss4lMJ0IwQXIm+zwTCmE/hoqt1nHZ81C3hlCyJ7Anq6pVOBE1PB3TfZpxeN8skmnljITxCrAVIoQIdNzLrOWecjll50Jg6FlcrgHb98JZwSpZQ9Ucm1434N31FEW3K6bf1PNTkrF7VzDMzpNmyXTDBidrjKjfsEdJKa+pGq2e/yqaDuiWcUlXW86fK1QsXhZoAupZ1M04/b8S0mSu9ArtS3VVYaY8ebnQ+AgTVkUfSazTqaks4rRR8z59avRa/GYmmfYPNOG3G+SbHdWXpjPJhwZbTq07oVWXLlM2mJ+zo6GKNZqhhSzhdmNyuZS1XDaQ2flRJJWMzTg+aBXhNSUv/KFxkNJf6Nv2DNBDIQkaWBp3mddO0Te9vOzhdBEj1m9wqQa0vWkyKbsbp64bTxuzjwlnYupLn+/35fOBNcdIHk3S0snUTYE1Xqub0+Bdx8mtz2vOn8Ioeav394qbNOG3Go9u1TSB2C4ZsZzBAFvRGaLgEKZXRKoeT0V3YdcbNfNTpelyMm4xfmdO+oI6vxm9U2k3192acNr39Zh3fVy2npSP0B/N89PdmOFVHbDsmnaHVhr8JUNhwLnpyO77a/dfmtN+2jkZuaTRazfhmnDa9/fOa0yN46qJZFBbSurkwWKLjfdBdDVEcdQa+5PlPKzll6mdtPL//+8hpv68y4vg3is+u+4Kbcdosk2oWR+Ytp8zSSD5HEjzuPQpnfaukC6u9/vpZ28Fph7xukfHy7FLYvFydshmnzWuOcpoMR5089FWUsIizh3Yej68p2EJOO6OPPSMQDJf68HU79JpwhcdyWrf9GMsNp3mXKYxxSXzNeNTGc6t91PpZDaf7a7E3+b047bfC4Wx9bUpwO2e1YduvOW3Xmodmw6mOYmp7sF16Ipm3TZJVS7F8Kxz/YslGTU5fvliJHwnGi/orcSp20qxuX9vvX9+MbRy2aY+0Ub114qHCcZx5KOZoGnGcooTQz/gQmjPP9y1rhYXX0NhgANOZRtsO//Swm9gT1L5GbZpdZ7p6M04vlof6/n6zdJWllHZRqdB84Ao0sKUVY36NUdgOTvtD0F05wN0XD9s5txabcdoUtJ3bL5gQ2YEeRXqYkJj//qI4e7wf6nt+hEbSmZG+6dNy2vfue3LQUQtNJ7ycd67ejNPPGjl9Xst4Bo+t70vRkt95NGKMbPODgkt1fCFx401vB6eDrn3Xn/Lb8fPa3+mvfn7sGMqzuveSQvOoRdFDS1rSWx6cyqyEFE0ad6eaMZ/t4HTghybdojZ64UOdUvYu3nCsr+H04k1zY9nEkvjS0mSzf4N6a9yw7qBKPWSjll9upvi3g9PhoH7PTNWCWre4wWrKDcf52+W8zVS0yOROfaOHlrSk2OkI4OIKXdUVgEeXIy/PnTwtp8OQm5tuQ7SrtMZfHAytbDjH1wyitIvOI4YzalH03aUJfMir/m0WI33dcHT/HbaD06VVZ9lSaa/rXg0eLPvbkNPLdqC/Top9piXShI7VgKWoUuxBxp+YD6yXqgfIKbaD0+Ulp933s0lC8/LDMYANOT2om/5es2aCFZm/t6rRYofmPGBzBkcOKxUPrD8lmHUetRWcLq+O7M0Gg5mSam0QDPcl2JDTzxuv/7YJDwV/t9HS0O8YmPPCtsgc9YOhMtXFHSW/HZyOxMN1haaIm04NXop23JDTdqT/9rRJk5kwamTwmm0buB/MFB5dtRrnIXTEdDs4pdtuDRB3HRm9McrLQ6qbcvqqGZpqV56H4Jc13XqzXopR6mEMdtL0itmDK6RrdLt7W8Hp6IB+dzbDr18cD2M8Nuf0XbtOup3QDBil6bUVzhzjQJcMVRCOPEzkF1rFWLjQMnq+yHZwOjZF+mFs+GckBMLakNO2e7rX2QghVNChLMtlGSizv5AtQJ086nhNsjMWb7QEv9tZfmJO54vil2Nfjiz4tEfCJ3qjA+s4fdMERk6Oe/l8WIwNpy5KxcHEvobGO/c9DEKFn5bTq4WBKMYa/0izG4vU6c14rl242rj93ZCzG/EaWZHplbJc4K+XfFSGTx9u/V4/cvBpOW1EcTR+Z2kufTZy0SAebN3unC9aQW3jYRPfbw0RXrZJ+MFYbsYeuHdPymln5dfoIt5BBI2/HPw0V4aCpaxZudoG8k3a0JOQKU6ayL1yOXK7Ez4x7vvjrwePeUpOuzsOMIcjmjDpN7ulNRRfZSOd8NJ0v1oRtXbfieRrt0A6ZOR2dHG2tEYa53mdsTKqBpYUUj3Hd/ZAXPTp+OkJj+X0yrPlBv1aL5p0u+kr9d+vXusTLS61V0wM+Xb9EFvpa7pWo04ums11r0Ugtakcbj7MNaBfKu5NNErp8mqZx8bvfyKnR2t3hKlh11PQPX+qafnrI0B60Pqctj4qqNR2ZY3GFO+b6iuX1u1mvGwhaXx6Co/Ecj12n4lP5DTdjNPGs+90wcuGnsdwOtACrzr7oXTUncbYRw2pcr+MpZeAuVwVHDkWHvc7c7qhnLa9peZ6vDyH8gs4beek4ZUu2+RDpojGuvaeEqEPnBiucFKHe4M8CafL/t8YirZbkjN26XlBKZttK34Ep7PhnhMvOtt3dMKjUYSxNyibF7lX10gvCqKhx8s5HoX9O3N6chQfPQx3fbR56B1uiCBayqnT+nvNH8lY/l7Gvu8XBYgfeCFzyV0/KnU4zHuBu4eMU22jXo7eflpvObO9m8kNcN06qX1JRdLRFF1JN8S/ZRPXNR9QU8XK7RdeHD/bCCt8qW/qNb8Ho19vI77t7tE7ed5bBxZD1+NrTgzKwn+oR2q2veCVO+r8efCuu2H5pLcNolXgB8mk0KRWqVxM9i6Xn/Inw8v9Lqn9vbXT8mFOi6Aj3AdE7G93knrXI3XvdW9d/ZG43jJ5ZndWYnFgyu1OUruboAIGxsIKzRXxethT8u7w87vmwJQ/jpH+zXDfP1pjf8iI4UjZwF/1D0PJ6W7Rga6fd7LYkYpe9A85mpzdjfnEN5Yb5WGYxTfDGXCQ0bv+QTI7nYruz/qkTo4fdw7EN4PzTm7P/uQ79BO8PO6fAzXZf7Yxq19+NjjC7+e94z/7dvIVXg3Oj5rsnd+9eXgTtuv7s73BnT//479/h/L+IXDQP0mG0nr66n7N4cXXL++e7y+dc7b/9ofVt/zZ8K/jpTMjJ5Nzcij0y+VY0G9f3l3So6QHN9y+/WJ31nEHwndvl8+NBNbOz8/Ozi6OX786ANy/eg1kAkaOPp5M/vrZ+PDSnxl34yfwdrZ2npB/I+dw0q8+7pr9CN6dbnT09jijO9u0AgfPzx9zAHcjyKf/88+nLvoW4+XrJWv+EKO3H9c5CDsQHLzdXAWAc/DxXw9nuQP68fnF2JHQy21+/+Pfnvg44z8Q3nz3+vKCmvhxZokvsP/vz75783BWO7QQfvjxu8u3hLyf6Y+fgd+ff67/3v/3dy+f/nD4Pyj++eKL/z09e0twfk5+nv37f1/9uOqEih0eAcH4v+m3J87Jo8+12mGHHXbYYYcdCKRgJro5CY+dBaVpICFXIoUE8RpKlulkxzjJjBSTm9G1nXopekksxApNqmN9XS8IJIQsLtIhla5MDfWI40zTimcRmTDOFT0lIRSBqLgSyvUsTJWMuEJppjtxFCkKNzP4LNI5RcsQzT4H4z6PsswNNbIGUg31EFIszeTCtF64PaclSDm6XjDVI8uNIg4+qm8djtNDyNFKlMw0NU2ir+sFeWyEiq7Pp6YOD9JIFLjKcZlBlih6QUr2C8q4rJrnZiMx0Kr8YlGcRbFqmRl5F1fhVgQqsUoRCXzpxyjyNcMKipicWRRRx8+qF3QqjJa4nM0iyS9TIfVLFWmM4rpaQH0ap/QtlOFMQCHjJclMJMsYWNkPXTfgkMkEJLdiRoIwZg6b+yYySiYlF0Ox2UBD8PzUjcsIJYyYuGEZIxFHeUGCqxLsIcejcQ9ukSA2s8Opmtn1guKMbnY21enWNyo8zbJl1zV9kZIeeYnCKImnI7sI8xw+WbPIWGvGSHyBYxLjEqhpSTckyH0X8fD6gk7ij3K69TupAi+wpgoNYlP8iOVNYEqhW1c5DLfCPc58UnmCls+rUwKCwkB6vc0BXkToxnQzj1SwbBrg50C9hZhu90YuZEV6DE7MZEglmbAxfaFZCR9OTM6kInFUSogsn0ZLufBTI5uUzeirZ/BGgU3ygZLQteOWgyLbQhLJTLDh6tQvQiKhJJ3KRrjYYGCuYVpqVSxMFQlRjqYiiZFICxHeV7BYlEM5VQnNSBjaXILXpYIt5vCi5EkF5B75hDIncJBnEyJzUoN1qIVMj3hVGAkopdKqw3vrZNs3c9UJbk5Z7W00n2qYBu+EwIyC1ZrTqiYSwimoh6wN7I9wCs2CPkVanNnge4ZBfs2qGhFBmvlsjtJZSEjlQiT6zXZ/MyJfZm7DF1lYcWqQeiOcxkBYBpwm5A/VhhwjhWMSJImOI/fjtsIoKkiekpKAdAlQPWpAl2JH9WZ3ebW/gwjSMQ9VoQjobugGjzzCqUM41XUNrrY8y1hEhfkyEha/ulVkkIHFadEJaAkKNlq5u36M6zMsSp8SKUHCEqcxLjXPT9GM7jQQySVHGq5W2lJV7CpYT7QllfG9WrhnWNTIK8SBFZGdy0NUkJ3pprrn5RWnHkiRQgQYBQxn0jIzNqcRUYpwlGFTqDk14Yq5NXNiumHgVJ9VkWy8GSP6cEkTIviKckpDW6Q6WGLBKSmML0J7bepEZGbaTCR3cxlbFhLIaby4qSwctLhQwZX2w3JMAxgcLZiRWmFkcWUsXYxr9j2fbmCakrdcltMM7I8ESjSuaukKRaCEJKr0oS4rTgMZanqmuspCTkEjJWDzYlD6HAYDg2y6259jFws5BeWQ4UgBSSBCkxO6iJwrCWmPUVmSfCpONTQN/FRzSOlIIRctwxUtQyQbn0iainTGDRtO0zryrJbT0mFdheXbcM4AJ3ESkvw4BbRwGYuOtHgRG2R/wWm22KoGe6lPCY+qjPM1Zzcanl19GmF1t072c8WkKhxpwWnK0rbPslZYPZQreRAkKKtqELl1qPICPkRElbJat32oJNUxUuAUTAMYHq5SHWXZcgpaitgbWgrVMCqpU3nS9g2ZSMR0wSlivUI05p5NisYv3kjMLSsna84Jp6DlggQ0K237YuH0OaXm0BG8kkrO1OroU+AUSYUdwNOr/TSxuGj7quVUetXC0dS2q/zoO8TrDhqsaGKDHBWkzc5tkRSOMheChiSUikZloyKy1SgpEgcSGFKRNWlQt0J/10HDTjtRdDPQp0gQLUmUyAOgrpBPWESlTQKg4BdaYxopZFWzIPa09cU6tVEuicyhNopwSiz6nCoLeNeqbl36ME1mkUVPNTRBLbLURmXNDll51bRmxNRMRWOhp7ykw6lC7SI5d0KnhJnkJemLJApUjkWrqGbKrUQvXnuuRogLRSF1zZdyphRQ+kTGchBgspeb7wUlyETA2GIgk0eJeJbrWGSdEpeiaBeVSOpYyT1sgDgyZR1OE/s+OL4FKFJMhYocjz33fCUxwfqnMiSGvk5uD0LyRE5RQA3puASLAT6T54Olgwc5USFbQkBfLCcnBMRFmceiTd5dsqksaVhDIT18WxUhK1vOoqAJcZ9ymAQdpUUxA40NIh8Wha7IOThmPvi0HJYty5NJ7i6RYJ3hcg/sO3hPRSCW5ExfcL7ykh6bHTNe7no0a2HGiL1tFwZgFVGp7HEuanCD4IZpmGWRJWRxkmVZrlpZmsMvlC1L0UyQuziCa6Lat0YGZ5K2wEdpXnPqJilY5dBAoZsTeVRpGWJFyRwkxImU827skueqBhunVg4AD96KczeXkBRbMUi5lKfwS+rEKeVoTlUMlK2SESlOgQZDcuK5JKXUq1NRallu0oYfz+Fm0AJJLOV56FIzkWm6g1g3TnODzSVXslyX5u5Qhadw5EWcXIrDMKTvIilK7e2EelapV961kgdOKtphhx122GGH7UMWiJ+M2YbQRmCSjc77MCmWkjtQRqBn+iqYg2duWl4CcWa2GCmKaa45EPsTIHwC2Cn7eEzHoK4CfDN6w2Z4sCy7Gdwddthhh98K0NnNozDMwuYw0FTPDJRqjTkTYmVp29gGBre8oy9BoofQzQ+jrD/Q4Or9jcCMbDi6wyZKNS1i5eHiWicMUxRr/c3VJX38wdsA3vRFIFVpt4mTSjLMVrQ8Rs3Y+PKogeGPDyP6Xp5hL4wGWxPpg5Fcw+NQH0K4mHiYc3hx4nPJBBIK7X5tpL6IthbVuLWaSwK4DTwZJ1KA0+mcyO3U4gUWSYWJ6BflDAmI5Z0pIi6QypNPnoUfLDunA1usA9eTsaM52fKITGW6ETLoeI8wtQwBpcAxTwaH4Vlz8kl+oKlB0iDnOdzlyItdE0NcjclnPhnnnsLdpIQGHVpSDWSToV3DmKItRMSYiZuDJMRlqc/IQWbAqaAUOhIiLReDWWzZRSZiBeVYlNhcizk7V3V7lsmyNc1sBUmel3FkIjrXXK6c1a1ZoNPDMZcqZYQsM3I9UZUYLwwKF+VlEAZ2glxvRkaWpVCOUCimWSC1nCo6re5QtIBTnpNT5JaiK8LnnNOlHOQ01vjc5Fe92BMiYgLF1MiENIbm5ckOlVMypk3GwKVCRJJdqtAAkQF/81h0I7mA701k0f9ACpmHF+FmuBYVXq1BBTIR4chBHpayKnpT5HJzCdSIWookW8EAsTc8GcVFiFgdOI3mIZDYcMqZaunzjuc6dC6WcVFaaMiwNaQUBmKLADRJNE2GB69tAyImhBZNBof9gEx9WpTTGORyGmCLzBSQtk84nQOnOUOOck/pDIKDQc8STmXg3CzIRF5u4Ha/UyKnMZNZliTNF5NnKejTqRgIFjQDg8hoIAMzCzUdRTnucqqRCdnMrKa6ybSSRNgvNYHciOwAqdGa/Y+eEqSBsaoaaWBXhIrTQkIJ4cYtsigV4FW0BaemEPuiwTtK6kJNWMR2EeLs0kAacGoFXCg1SzMMIqdSEVhzJ5OCMuWt0CH6VA0CQYLqmZOVBcCpixXekXK+nKkJzoDThdkyAzIzVE6hIkwyGeRCZhFSZQ3NsMROCw+lZOXGummhJ4JjlmLu6kGRq3aQTj0vVkU5FDJ5NlW9witL0chLj7UCOYZ3mUmxjQs7RDpIU1jOWFcOLLYMYhSULtJ8r/TExUyQo0CzZ1Eu40LOQOdin+hMm5tKXsDHpcamXqBKYgm8yNgG5rViFpWFlHjVshyJPBEFKbhrciAJuq2DPtVQ7AXIEX1T9zwr8pxEXLNf9VOBt1hLstLUQY7j8IbFw3/HAoNvqaHoAmxd5S1j7vAOYsmKGj4PecRac0uFJBWum6two2o588TL4fpg4Xg5qWERoVXzkLbthBytB5dPecsBUbemc4dk6zjkEpcsxHFBnbiQmUXMjuBYTrVlFC9BiVi4EzwO+t+gmRmqwEppupV2fzVMxtMVkdt4KitiPCXTVq1124EiNjXlMaODkqIp29u72WGHHXb4TfD/AvR0bxXkZUIAAAAASUVORK5CYII=">
        <span class="md-title" style="color: aliceblue; align-items: center;">Know Your Events </span></div>
       

       
        <md-icon class="bt-primary"></md-icon>
        <img style="height: 5%; width: 10%; margin-right: 90px;">

        <div style="flex-grow: 1; display: flex; justify-content: center;">
          <input type="text" v-model="searchTerm" placeholder="Search..." 
                 style="padding: 8px; border-radius: 4px; border: none; width: 300px;"/>
                </div>
      </md-app-toolbar>
      <md-app-content >

      <div class="bodycontent" >

        <md-card v-for="item in filteredItems" :key="item.id" :item="item">
      
        <md-card-area>
          <md-card-header>
            <md-card-media style="height: 100%; width: 100%; margin-left: 0%; padding-bottom: 5%;">
              <img :src="item.poster">

        </md-card-media >
            <span class="md-title">{{item.eve}}</span>
          </md-card-header>
           <md-card-content>
            <p class="txt">DATE: {{item.date}}</p>
            <p class="txt">VENUE: {{item.venue}}</p>
            <p class="txt">Contact: {{item.phone}}</p>
            <a :href="item.link" class="txt">
                <md-button class="" style="color: aliceblue; font-weight: 500; ">Register</md-button>
            </a>
        </md-card-content>
        </md-card-area>
    </md-card>
  </div>
      </md-app-content>
    </md-app>
  </div>
</template>

<style>
  .md-app-toolbar 
  {
    color: aliceblue;
    background-color: #397bbd;
  }

.md-card{
  margin-top: 20%;

}
.md-card:hover{
 box-shadow: 0px 15px 30px rgba(209, 94, 0, 0.977);
}
md-app-toolbar{
  background-color: #397bbd;
  color: #343a40;
}
  .md-title{
    color: black;
    font-weight: 1800;
  }
  .txt{
    color: rgb(19, 8, 8);
    font-size: medium;
    font-weight: 500;
    font-size: 18px;
    
  }
  .md-card {
    width: 320px;
    margin: 4px;
    display: inline-block;
    vertical-align: top;
  }
  .md-card-media{
    width:100px;
    height:150px;
  }
</style>
<script>
export default {
  data() {
    return {
      items: [], // Data fetched from the API will be stored here
      searchTerm: '' // Search term for filtering movies
    };
  },
  mounted() {
    this.fetchData();
  },
  computed: {
    filteredItems() {
      if (!this.searchTerm) {
        return this.items; // Return all items if no search term
      }
      const lowerCaseSearchTerm = this.searchTerm.toLowerCase();
      return this.items.filter(item => 
        item.eve.toLowerCase().includes(lowerCaseSearchTerm)
      );
    },
  },
  methods: {
    async fetchData() {
      try {
        const response = await fetch('http://127.0.0.1:8005/api/data/');
        const data = await response.json();
        this.items = data; // Assuming API returns an array of items
      } catch (error) {
        console.error('Error fetching data:', error);
      }
    },
    Homepage() {
      this.$router.push('/');
    },
  }
};
</script>
