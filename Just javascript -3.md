## A Story

故事开始于夏洛克侦探，住在伦敦的世界著名侦探。

```javascript
let sherlock = {
  surname: 'Holmes',
  address: { city: 'London' } 
};
```

他的好朋友约翰华生最近搬来和夏洛克一起住

```javascript
let john = {
  surname: 'Watson',
  address: sherlock.address
};
```

 夏洛克虽然是个出色的侦探，但是他不太好相处， 直到有一天华生受够了，他改了姓并且搬到了Malibu.

```javascript
join.surname = 'Lennon'
join.address.city = 'Malibu'
```

那么问题来了，现在华生住哪？夏洛克呢？（如果你不太确定，用纸和笔写下每一行发生的事情的心智模型）

```javascript
console.log(sherlock.surname); // ?
console.log(sherlock.address.city); // ?
console.log(john.surname); // ?
console.log(john.address.city); // ?
```

.
.

.

.

.

.

.

.

.

.

.

.

.

.

```javascript
console.log(sherlock.surname); // "Holmes"
console.log(sherlock.address.city); // "Malibu"
console.log(john.surname); // "Lennon"
console.log(john.address.city); // "Malibu"
```

 看起来夏洛克没那么好摆脱，他跟着华生一起搬去了Malibu 😲。

## 属性

```javascript
let sherlock = {}
```

![图片](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAwQAAAEUCAIAAAAa0GYHAAAgAElEQVR4Ae3BT0wjiYIf4B/VtsGuyp/VtoeaRHr2ysXFe7CR4B2CeR7lVPQ75GJ2VorU7X69F1YQt/QmGiNGPA0KgifNSOOAhstM2j2nzFLXQN2yFuayoLQdJb5Q1tpaadses9lNtsoGTE8laamlboEb6MbGdP2+b8C2bRARERE5lQAiIiIiBxNARERE5GACiIiIiBxMABEREZGDCSAiIiJyMAFEREREDiaAiIiIyMEEEBERETmYACIiIiIHE0BERETkYAKIiIiIHEwAERERkYMJICIiInIwAUREREQOJoCIiIjIwQQQEREROZgAIiIiIgcTQERERORgAoiIiIgcTAARERGRgwkgIiIicjABRERERA4mgIiIiMjBBBARERE5mAAiIiIiBxNARERE5GACiIiIiBxMABEREZGDCSAiIiJyMAFEREREDiaAiIiIyMEEEBERETmYACIiIiIHE0BERETkYAKIiIiIHEwAERERkYMJICIiInIwAUREREQOJoCIiIjIwQQQEREROZgAIiIiIgcTQERERORgAoiIiIgcTAARERGRgwkgIiIicjABRERERA4mgIiIiMjBBBARERE5mAAiIiIiBxNARERE5GACiIiIiBxMABEREZGDCSAiIiJyMAFEREREDiaAiIiIyMEEEBERETmYACIiIiIHE0BERETkYAKIiIiIHEwAERERkYMJICIiInIwAUREREQOJoCIiIjIwQQQEREROZgAIiIiIgdzgYiIiM5jWU3bttHBwMCAKPpAt58LREREzmZZTQCi6MNLzWbr4OCvAZhm8+Cggg5k2f/xx34AIyN/5PN58ZJlNQGIog90e7hARETkMO12++SkLYo+APX6oWFUDg4qhlGt1RqGUcE7UZSgLPsVJTAyElSU4PDwXQCW1fR4PG63C9THBmzbBhERkQO0Wkde7xCAcrn67FmpUCgVCiXTtNAFkiQqSiAaDY+OhiORMIBW68jrHQL1nwHbtkFERPTharWOvN4hy2rt7PxVoVDK5/dN00IPSZIYjYZjsbHJyV+KoteymqLoA/WNAdu2QURE9MFptY683iEAup7L5/fz+T30gVhsPBYb+9WvfunzeY+OjoeGBkE3bcC2bRAREX1ATk7aHo+7XK5ubm7l8/umaaHPSJIYi41NT98LhQLHxyeDgx7QzRmwbRtEREQfhFbryOsd0vWcrucKhRL6nqIEE4kpVY2326dutwt0EwZs2wYREdEt126fut0uXc9ls1qt1sCtIsv+ZDLxq1/90v3/uUC9NWDbNoiIiG6t4+OTwUGPrueyWa1Wa+DWkiRxdva+qsZbrSOvdwjUKwO2bYOIiOgWarWOvN6h3d39tbWntVoDHwRZ9ieTCVWNt1pHXu8QqPsGbNsGERHRrXJy0vZ43PX64crKt4VCCR+caDQ8N/cgFAq022232w3qpgHbtkFERHR7nJy0PR53Nqtlsxo+aInEvYcPp12uO4ODHlDXDNi2DSIiotvg5KTt8biLxdLKykat1oADyLJ/fn4mEgm322232w3qggHbtkFERNT3jo9PBgc92ayWzWpwmETi3uzs/ePjk8FBD+i6Ddi2DSIiov7Wbp/+r//1DwsLXxlGBY6kKMH5+Zlf/OJfuN1u0LUasG0bRERE/er4+GRw0LO7u7+ysmGaFhxMksT5+ZmJibGTk7bH4wZdkwHbtkFERNSX2u1Tt9uVzWrZrAZ6KZG4Nzt7v9U68nqHQNdhwLZtEBER9Z/j45MXL178x/+Y1fUc6DWx2Pj8/J+7XHcGBz2g9zZg2zaIiIj6zPHxyenpi1TqS8OogM5QlGAm8ztBGPB6h0DvRwAREVGfsazm6emLVOpLw6iAzmMYlVTqy7/923q7fQp6PwO2bcNJarVGPr9nGNXnzxsgcoyRkYCiBGOxMUkSQdTf/vEfzZ9++ruVlQ3DqIDeSpLETGbxF7/4l263C/SuBmzbhmOsrz/VtO3h4buKEhwZCYLIMZ49KxlGBcDc3ANVjYOoX/3jP5o//fR3qdSSaVqgS5AkMZNZ/MUv/qXb7QK9kwHbtuEMq6sbOzt7Dx8mEol7IHIe07SyWU3TttPpGVWNg6j/HB+fnJ6efvrpnGlaoEuTJDGTWfzooz/8J/9EAl3dgG3bcABdz62ubnzzzWI0GgaRg2WzWjar/ef/vCbLfhD1k+Pjk9PTF6nUl4ZRAV2RJIk//rjuct0ZHPSArkiAM2xubqlqPBoNg8jZksnE8PBdTdsCUT9ptY5OT1+kUl8aRgV0daZppVJfnp6+aLWOQFckwBnK5aqqxkFEwNTUJwcHVRD1jXa77fUOrax8axgV0LsyjEoq9aXXO9Run4KuQoADFAolAIoSABER9R+3272+/kM+vwd6P4ZRWV3dcLtdoKsQ4BiSJIKIiPrMyUlb13OatgW6Drqe07Rt0FUIICIiuiGt1tHf/M3frq//ALo+6+tPy+Xq8fEJ6HIEEBER3YR2+/Tnn+2Fha9M0wJdq4WFr05PXxwdHYMuQQAREdFNcLtda2vZWq0Bum61WmNl5duhoUHQJQggIiLquXa7vbu7r+s5UHfk83uatn1y0gZdxAUiIqLeOjo6fvHi55WVDdyQaDSMDgyjapoWrkiSREUJoINCoYSbkM1qk5Pjf/AH/8zjcYM6c4GIiKi3hoYGv/jia9O00Cuy7FfV+OhoOBIJ463K5WoqtWSaFi5NksRMZjEUCuCtisXSs2clXc/Vag30hGlaKyvffvPNIuitXCAiIuqh4+OT/f3/ns/voSdk2T8/PxOJhHE5oVBgfn5mYeErXNr8/EwoFMBFIpFwJBJOJhPFYmlt7QfDqKD7CoXS7u7+L38ZdbtdoA4EEBER9crJSfvFixdra0/RE6oa//7730ciYVyFJPlwFZLkw1VEIuHvvltV1Th6YmVl4+Sk/f+AOhBARETUQ3/xF/+lVmug+1Q1nk7PiKIPfSmdnpmdfYDuM01rc/O/uN1uUAcCiIiIeqLdPv2Hf/g/mraN7ovFxtPpGfS3RGJKVePovmxWq9cPj46OQecRQERE1BNut+s//ae/ME0LXSZJ4vz8DG6DubkHsuxH9z15sjk0NAg6jwAiIqLua7WO6vVDXc+h+2Zn74uiD7eBKPqSyQS6T9dz9frhyUkbdIYAIiKi7vN6h5482UT3SZKoqnHcHqoal2U/uu/Jk02Pxw06QwAREVGXtdun9fqhrufQfaoax3uwrOba2g+4irW1HyyrifcQi42j+3Q9V68ftlpHoDe5QERE1GVut+vJk030xOTkGC5hd3f/4KCCM/L5fcOo4CoMo5JKLcViYzhjZCQ4MTGGi0xNxTVtC9335MlmOj0DepMLREREXWZZrXx+Hz0RiYRxkS+++Dqf38P1MYyKYVRwHkUJfvfdKt4qFAqgJ3Q995vf/Mkf/ME/dbvdoFdcoL6USi3hPHNz9xUliA/L+vrTg4MqzpiaiqtqHLdNKrWE88zN3VeUIIicp9U62t7+S9O00H2y7MdFdD2Xz++hVwyjomnbicQU3ioaDRcKJXTf1tZ//bf/9t+AXuMC9aVisYTzmGYTH5yDg2qxWMIZo6Nh3ELFYgnnMc0miBzJ6x3StC30hCz7cRFdz6G3dD2XSEyhP+h6LplMgF4jgIiIqGuOjo6LxVKt1kDfKBRK6C3DqOAiihJET9Rqjd3d/VbrCPSKACIioq4ZGhrc3s6hVxQliNtJknzole3tnNc7BHpFABERUTfl8/voFUnyoS8ViyX0jXx+z7JaoFcEEBERdYdlNXd3903TQt8ol6sgYGfnryyrCXpJABERUXeIom9nZw/9xDQtEJDP74uiD/SSACIioq7J5/dB/Sef3wO9IoCIiKgLWq2jYrFkmhaoL+3u7ltWEwQIICIi6o5nz0qgfvXsWcnjcYMAAURERF3g9Q7l8/ugflUolNxuNwgQQERE1B2GUQH1K8OoWFYLBAggIiK6bq3WUbFYAvW3QuF/Hh0dw/EEEBERXbeff/752bMSek6W/bidRkaC6LmDg4pt23A8AURERNdNFH2GUUXPjYwEcTspShA9VyiUvN4hOJ4L1E2maeXz+zs7e7Vao1yu4pVIJPzxx/5oNByLjUmSiKur1Rr5/N6zZyXTbOKVkZFANBqOxcZxFfn8XqFQOjioGkbFspp4aXj4rix/NDISUNW4ogTxVqZpGUYVZ0iST1GCeMkwKvn8/rNnJbw0OhqWZb+qxvHearVGoVAqFErPnzeKxRJeGR6+K8sfjY6Go9FwNBrGOzFNK5/fLxRKz583isUSXgmFAiMjwWg0HIuNSZKI92CalmFU0ZmiBCRJBNFtYxgV9JYs+0OhAN7q+fMGbsLBQTUSCaOz4eG7ihI0jAp6yDCqIMAF6ppsVtvc3LKsJs4oFkvFInQ9B0BV48lkQpb9uBzTtLJZTdO2cUaxWNK0bVH0PXyYSCTu4SLZrLa5uWVZTZxRrx/W64fFYknTtoeH7z58OK2qcXRgGNXHj5dwRiQSzmQWTdNaWdnY3d3Ha4rFUiIxBcTxHgqF0ubm1u7uPs5Trx/W64fFYgnA8PDdqalPEokpSRJxOaZpadr25uaWZTVxRrlcLZerup4TRd/c3ANVjeOdmKaVSi2Vy1V0EAoFMplFEN1CtVoDvaWqcVykVmvgJtRqDVwkkZhaXd1AD5mmZVktUfTC2VygLjBNK5VaKperuARdzx0cVL7//ve4BNO0UqmlcrmKziyrub7+g2FU0+kZdGAYlZWVjXK5ikuo1w9XVze2t3PLy7+VJBFXYZpWKrVULldxhiSJeFemaa2sbOzu7uNy6vXDbFbb3Nyan5+JxcZxkUKhtLDwlWU1cRHLatZqDbwT07RSqaVyuYoOQqFAJrMoSSKIbptisYTekmX/9PQ9XKRQKOEmFAolXERV49msVqs10EOG8deRSBjOJoC6YGVlo1yu4tLm5h7gclZWNsrlKi5B13PZrIbzGEYllVoql6u4imKxlEotmaaFq1hY+LpcruJaGUbl0aPPd3f3cUWW1fzii6/X15/irXQ99/jxkmU10U2maaVSS+VyFR2EQoFMZlGSRBDdBrqeW1j46te//s0nn/yprudMs4neWl7+TBR9eCvLahYKJdwEw6jU64e4yPLyZ5IkooeeP2+YpgVnE0DXrVAo7e7u49ISialoNIzLsawmLi2b1Wq1Bt5kmlYqtWRZTVxduVxNpZZwacViqVgs4VrVao1UaqleP8S70rTt9fWn6CCf31td3UCXmaaVSi2Vy1V0EImEM5lFSRJB1PcMo/Lpp7Orqxu7u/uW1QTw8cf+g4MKekWSxOXlz0KhAC6yvZ3Dzdne/ktcJBQKZDKLkiSiV2q1BhxPAF23zc0tXJoo+pLJBLpG07bwpoWFry2riQ6Gh+9GIuFIJIwOyuVqNqvhOsiyH1e3sPCVZTXxfjRtO5/fwxm1WmNlZQNdZppWKrVULlfRgarGM5lFSRJB1Pd0Pfdnf5au1w/xGln+CL0SjYYzmcWJiTFcgqZt4eZo2rZlNXGRUCjw/fe/j0bD6IlarSFJIpzNBbpuu7v7OI+qxmOxsVhs3DStfH5/eztXLJbm52ckSUTXPHtWwmsKhVKxWMJ5QqHA3NyDaDSMVzRt68kTzbKaeFM2q6lqXJb9eD+y7McVZbNauVzFdVhZ2fjxx7AkiXjNysqGZTXRTaZppVJL5XIVHahqPJ2eAdFtoOu51dUNnDE8fLdQKKGbotGwogQnJ8cikTAuR9O2a7UGbo5pWpubW8lkAhcZHr77zTeLxWJpZ2ffMCqFQgldU6s14Hgu0LUyTQvnEUVfOj2DlyRJVNW4qsYNo6IoQVzdxMTYw4cJRQkCyOf3njzRyuUqzlMuV/GaJ080nCcUCmQyi5Ik4jWJxL1oNJxKLVlWE2/StK3Z2Qe4ilAoMDk5Lsv+Wq1RqzV2dvZwRaZpbW5uobNEYkpV44oSBGCaVj6/v7m5VS5XcR7LamradjKZwCuGUSkWS+hAFH3T0/dUNS7LfgCmaRUKpc3N7WKxhEszTSuVWiqXq+hAVePp9AyIboNarbG29hQ3IZ2eUdU4rqJeP8xmNdw0TduemvpkePguLiESCUciYQC6nltd3QB1jQt0rWq1Bs5jWc3V1Y3Z2fuSJOIVRQni6hKJqdnZB3glFhuPRsOPHn1erx/iPLVaQ5b9AGq1RrFYwnnm52ckScQZihKcnr6XzWp4087O3uzsA1yOKPrm52disXG8Znb2Pq4on9+3rCbOI4q+TGZRUYJ4RZJEVY2ranx1dUPXczjP9vZfJpMJvKJp2+ggFAosL38my368IkliLDYei43n83um2cQlmKaVSi2Vy1V0oKrxdHoGRLdENqtZVhM9l0jcU9U4rmhh4SvTtHDTTNNaWPgqk1kURR8uTVXjhlHVtC10Qa3WgOO5QNdKUYLoQNdzup6bmBibnByPxcYkScTVDQ/fnZ19gDdJkvjw4fTq6gbOU6s1ZNkPIJ/fw3lCoYBpNguFEs6jKAGcUa8f1moNWfbjEubnZ2KxcbxJkkRc0c7OHjpYXv5MUYI4Tzo98/x5o1gs4Yx6/dAwKooSxEs7O3s4jyj6lpc/k2U/zhOLjeNyVlY2LKuJDhKJqdnZByC6JUzT0vUczhONhgEYRhXdIUk+XIVlNdfWnhpGBf3BMCqp1FImsyiKPlyaJPnQHbVaA47nAl23UChQLlfRwe7u/u7uPoBIJDw1FVfVOK5iauoTnCcaDeMihlHFecrl6uPHS7giw6jIsh8XiUTCsdg4rkOhUMJ5JibGotEwOpubu/9nf5bGeQqFkqIEAdRqDctq4jzT0/dk2Y/3ZllNdJBOz6hqHES3Rz6/j7cyTQt9wLKaqdSSYVTQTwyjkkotLS9/Njx8F9QHXKDr9vBh4osvvsZFisVSsVh68mRzfv7Po9EwLicaDeM8suzHRZ4/b+D6GEY1FhvHRaanp3AdTNOyrCbOMzk5jrdSlODw8N16/RBn1GoNvFSrNdBBLDaGbkqnZ1Q1jt4yTatQKIHoXRUKJfS9crmaSi2ZpoX+YxiVR48+z2QWQ6EA6Ka5QNctFhtX1biu53AJ9frh48dL6fSMqsbxIYpGw7gOhlFFB7Lsx0Vk+aN6/RBnHBxU8VKt1kAHihLEB6dcrj5+vASiD1ooFMhkFhcWvqrVGugzkiQuL/82FAqA+oAA6oJ0eiaZTODS1tae1moNfHBE0SdJIm4D07RwQ1ZXN3Q9ByLqglAo8P33v1eUIPqJogR//HEtEgmD+oML1B3JZEJV49mspus5XMSympq2NTv7ADdhePiuLH+EK5JlPy6iKEFcE1n2owPTtPCuPv7Yj5cUJYgOarWGLPvRTWtrTxUloChB9EokEs5kFkH0rrJZLZvVcBuIoi+TWXz06PNarYE+IEliJrMoij5Q33CBukaW/en0TDo9k8/v5fP7z579z3r9EB0cHFRxQ6amPkkmE+hvsuxHB/n8fiw2js5M0yoWSziPLPtxkUKhpKpxvLdQKFAuV3Eey2qmUkuZzKKiBEF0GyhKADdE07YnJ8dDoQAuTRR9y8ufPXr0OfrA8vJvRdGHqyiXq5q2DeoaAdR9sdh4Oj3z44/r33yzKIo+nKdYLKHLRkfDOM/BQQW3QSQSxnl2dvZqtQY6y2Y1dKAoAbwUjYbRwZMnm6Zp4b3NzT1Q1Tg6sKxmKrVkGBUQ3QbRaFgUfehMlv3oDtO0UqmlbFbTtO16/RCXEwoFkskEbloicS8SCeNy6vVDXc9ls1oqtWSaFqhrBFAXZLNaPr+HM6LR8PT0PdwQRQngPLu7+7VaAx1ks1o2q2Wzmq7nCoVSoVDCDZmcHMN5LKu5sPCVaVo4j67nNG0b5xFFXyw2jlcmJsZwnnr9cH39B3RQqzUKhRIuZ3b2figUQAeW1UyllkzTAlHfkyRxcnIc5ykUSgBk2Y+uMU0rm9XW159++uns6uqGZTVxCdPT9yRJxM2RJPHhwwQuwbKa6+s/fPrp7OrqRjarmaaFrpFlPxxPAF23QqGUzWpffPH1wsJXpmnhTbVaA+eJRMLoslhsXBR9OM/CwlemaeGMQqGUzWrZrJbNaqurG48fLz1+vPTJJ3/6ySd/Wqs10Fux2Dg6KJerjx59XiiU8BrTtNbXn66ubqCDyclxvGZychwd6Hru0aPPC4USXmOaVjarPXr0eaFQwuVIkpjJLIZCAXRgWc1Uask0LRD1vdnZ+6Low03T9dyjR5+Xy1VcRBR9icQUbo6qxkXRh4uUy9VUaknTttATsuyH47lA121l5Vu8tLu7/+mnc1NT8Wg0LEmiYVQMo6rrOZzn44/96L7p6XvZrIYzyuXqo0efP3w4HYuNSZIIoFZr6Hpuc3ML54lEwrLsR2/Jsl9V47qew3nq9cPHj5eGh+/K8kd4qVgs4a2SyQReo6rxJ0826/VDnKdcrj5+vDQ8fFeWP8JLxWIJVydJ4vLyZ48efW5ZTZynXK6mUkuZzKIkiSDqY5IkLi9/9vjxEm5ardZIpZYymcVQKIC3mpr6JJvVcEOmp+/hIvX6YSq1ZJoWqIdcoGuVzWr1+iFesaympm1r2jYuEouNofsSianNzS3LauKMev1wdXUDl/PwYQI3YXb2/s7OnmU10UG9flivH+ISksmELPvxprm5B1988TU6q9cP6/VDvB9Z9mcyi6nUkmU1cZ5yuZpKLWUyi5IkgqiPRaPhdHpmbe2pZTXxmnK5Go2GC4USesU0rZWVje++W8VbDQ/fVZSgYVTQc7LsHx6+i4usrHxrmhZ6SJb97Xbb7XbDwQTQ9anVGtmshqsbHr4bi42j+yRJnJ+fwftR1Xg0GsZNkCRxfn4G7y0UCiSTCZwRi40nElPoPkUJZjKL6Kxcrq6sbICo76lq/Pvvfx+JhPEa07TQc4ZR0fUcLhKNhnETotEwLqLruUKhhN6SZf/x8QmcTQBdn7W1p3gn8/N/jl6JxcbT6Rm8q1AoMDt7HzcnFhtPp2fwHkKhQCaziA5mZx+oahzdpyjBdHoGne3u7q+uboCo78myP5NZ/O671URiKhIJA3j+vDE6GkbPado2LqIoAdwEWfbjIrqeQ8/Jsv/OnTtwNhfo+szPzywsfF0slnAV6fRMNBpGD6lqHMDq6gauKBIJLy//VpJE3ChVjcuyf2Xl23r9EFeUSEwlkwlJEtFZOj0jST5N20aXqWocwOrqBjrQ9RyAdHoGRH1PUYKzs0G8Ui5X0XOGUanXD4eH76Kzjz/24yaMjobxVpbVLBRK6LmPP/Z7vUNwNgF0fSRJzGQW0+mZ4eG7uITh4bv/4T/8VlXj6DlVjX/33WooFMDliKIvmUxkMouSJKIPRKPh77//fTKZEEUfLicSCX/zzeLs7ANJEnGR2dkH33yzGAoFcAmS5MO7UtV4IjGFznQ9t77+FES3TSgUwE0wjApuJ8Oo4CaMjPwRHM8Fum6qGlfVuK7ndnb2CoWSZTVxRigUmJqKq2pckkScJ5lM4Dyy7EcHyWQC55FlP86jKMHvv/99oVDS9dzOzp5lNXGeiYmxycnxWGxMkkR0IMv+ZDKBM2TZj0uYmoqPjoZxRjQaRmeSJCaTiURiKp/f39nZKxRKltXEGaFQYHQ0rKpxRQniKqLR8Pff/75QKOl6bmdnz7KaeJMo+iYnx1U1Ho2G8ZpkMoHzyLIf55mdfSDLftNsojPTtCRJBNGtoihBw6igtw4OKhMTY7iFnj0roedk2e/zeeF4LlB3qGpcVeMATNMyjCpeE42GcZFkMoErSiYTuLpoNByNhtPpGdO0DKOK18iyX5b9uARZ9ieTCbwrVY3jXUmSqKpxVY0DME3LMKp4RZJ8ihLE+4lGw9FoOJ2eMU3LMKp4RZb9suzHeZLJBK4okbgHog+OLPsNowLqY7LsBwEuUJdJkhiNhtH3JEmMRsO4zSRJjEbD6A5JEqPRMIjockzTikbD+fweqI9Fo+Hj45PBQQ+cTQAREdF1Gxz0jIwEQP1tdDT8888/w/EEEBERXTe32x2JhEH9TVH+yOsdguMJICIi6o5oNAzqV4oSFEUvCBBARETUBa3WUTQaBvWraDTcbrdBgAAiIqIucLlck5PjoH41Oho+PX0BAgQQERF1gdvtCoUCkiSC+o8kiRMTY17vEAgQQERE1DWx2Bio/0SjYdArAoiIiLrDspqTk+PoJ7L8EQiIxcZarSPQSwKIiIi6QxR9ExNjkiSibwwP34XjSZL4q1/90usdAr0kgIiIqJtisTH0imk20ZcikTD6Riw25vN5Qa8IICIi6ppW62h6+h56xTAquIgkieg/ptlEr0xNxS2rCXpFABERUdd4vUOhUEBRgugb0WgYvRWNhnERw6igJ2TZH4mERdEHekUAERFRN7VaR4nEFHqiVmvgIlNTcfTW9PQ9XMQ0m+iJROJeu30Keo0AIiKibvJ6h371q19Kkojuq9UaltXEW01MjCUS99ArqhqfmBjDRQyjgu6TJHFq6hPbtkGvcYGIiKjLXC5XIjGVzWrovkKhNDExhreanb0/NRXf2dnDGYZRzef3cEWKEozFxnDG5OR4KBTARYrFEnoiFhsTRS/oTS4QERF12cDAwPT0r7NZDd23s7M3MTGGi4RCgVAogPOsrm7oeg6XpijBTGZRFH14Vzs7++iJhw+nW60jr3cI9BoBREREXeZ2u0TRq6pxdF8+v29ZTbyHqak4rmJu7r4o+vAedD2H7lPV+PDwXa93CPQmAURERN3Xbp/+5jd/gu4zTWtzcwu3h67nTNNC9z18ON1qHYHOEEBERNR9brfro4/+MJlMoPs0bduymrgNLKu5vv4Duk9V48PDd73eIdAZAoiIiHqi3W5PT/9akkR0mWlaKysbuA1WVjZM00KXSZI4N5dst09B5xFARETUE+7/z5VMJtB9+fze6uoG+tvq6ih5u0EAAAjdSURBVEY+v4fuSySm3G6X2+0CnUcAERFRr3g87kRiSlGC6D5dz33xxdeW1UT/sazm6uqGrufQfbLs/5M/+TWoMwFEREQ9dHLSnpu7j57I5/c+/XRO13O4CtNs4ipMs4mr0PXco0ef63oOPTE/P3Pnzh2Pxw3qwAUiIqIe8njckUg4kbinaVvoPtO0Vlc31td/UNX46GhYUYLDw3fRWblcXVnZwFWsrGxkMouhUACdWVazUCg9e1bK5/dqtQZ6JRYbj0TCoLdygYiIqLfa7fbDh9P5/F6t1kBPmKalaVuatoUuME3r0aPP0X8kSZyf//Ojo+OhoUFQZwIcQFECAAqFEoiIqA+43W6X6878/Ayom+bnZzwe19DQIOitBDiAJInDw3cLhRKICNjZ2fv4Yz+IbtTgoCcSCScS90DdoarxiYkxt9sNuogAZ5ia+mRzc6tWa4DI2XQ9Vy5XVTUOopvWbrdnZ+8rShB03RQlODeXbLdPQZcgwBkSiSlZ9i8sfGUYFRA5la7n1taeqmo8Gg2D6Ka53e7j45Pl5c8kSQRdH0kS5+dnBGHA7XaBLmHAtm04g2laqdRSuVydmBgbGQmCyGF2dvbK5aqqxtPpGRD1jXa7/Vd/VVxY+Ap0TdLpmX/9r/+Vx+MGXc6AbdtwEl3Pra099XjcHo8bRI7h8Xj++I9HVDUejYZB1H+yWS2b1UDvLZG4Nzt7H3QVA7Ztw2E++eRPQeQwqhpPp2dA1MdWVzd0PQd6D6oaT6dnTk7aHo8bdGkuOE8oFCiXq6CLDA/fleWPcAmS5BsZCaJvmKZ1cFDFJRSLJThDNBoGUR9rt0/T6ZlarVEolEDvRFGCc3PJdvvU43GDrmLAtm04TD6/98UXX+N2CoUCkiTijNHRMM6jKAFJEnEeSfIpShDUgWlahlHFGaZpGUYVbzJN6+CgijcViyX0h+Hhuz/+uA6i/mZZTWAglfrSMCqgK1KUYCbzO5frzuCgB3RFA7Ztw3myWS2b1dBloVBAkkS8aXQ0jDdJkk9RgjgjGg2DPiyFQgmvqdUatVoDr9RqjefPG3ilVvupXj/EexNFXyazqChBEPW94+OT09MXqdSXhlEBXZqiBDOZ37lcdwYHPaCrG7BtG45UKJSePNGKxRJeMzx8V5Y/wptGR8N4k6IEJEnEayTJpyhBEHWNYVRMs4mXTNMyjCpeefashFcMo2JZTbwkir7JyfHZ2fuSJILoljg+Pjk9fZFKfWkYFdAlKEowk/mdy3VncNADeicDtm2DiIiobxwfn5yevkilvjSMCuitFCWYyfzO5bozOOgBvSsBRERE/WRw0ONy3clkfqcoQVBnihLMZH7nct0ZHPSA3sOAbdsgIiLqM8fHJ6enL9bWsrqeA50RjYaXl/+9y3VncNADej8Dtm2DiIio/7Tbp263a339B03bAr1GVePp9IxlNUXRB3pvA7Ztg4iIqC+12223263rudXVDdBL6fSMqsbb7VO32wW6DgO2bYOIiKiPnZy0/+Zv/nZh4atarQEHkyRxefm3kUgYdK0GbNsGERFRfzs+Pjk9fbGy8m0+vwdHikbDy8v/3uNxu90u0LUasG0bREREfe/o6HhoaFDTtrNZzTQtOMns7INEYqrVOvJ6h0DXbcC2bRAREd0SJyftv//7/72y8m2hUIIDKEpwfn4mFAqAumbAtm0QERHdHq3Wkdc7pGnb2axmmhY+UJIkJpOJRGKq1TryeodAXTNg2zaIiIhum5OTdrt9uraW1fUcPjix2Pi/+3fJf/7P/6nH4wZ12YBt2yAiIrqFWq0jr3eoWCw9eaIVCiV8EKLR8MOHiUgkfHR0PDQ0COq+Adu2QUREdGuZpiVJYrFYWlv7wTAquLVk2Z9MJlQ13modeb1DoF4ZsG0bREREt9zJSdvjce/u7m9ubhUKJdwqihJMJKZUNX5y0vZ43KDeGrBtG0RERB+Ek5O2x+MuFkvb2zldz6HvxWLj09NTkUj45KTt8bhBN2HAtm0QERF9QFqtI6936Kef/m5r67/qeq5Wa6DPyLJfVeNTU58MD99ttY683iHQzRmwbRtEREQfnHa7DQy43a5isbS9ncvn903Two2SJDEWG5ucHJ+YGGu328CA2+0C3bQB27ZBRET04To6Oh4aGgRQLJZ2dvbz+b1arYEekmV/LDY+OhqemBgDYFlNUfSB+saAbdsgIiJygFbryOW643a7f/rp7/7bf/sfhULJMKqGUUEXKEpQUQLRaHh09I+Hh++22+0XL34eGhoE9Z8B27ZBRETkMK3Wkdc7hJeKxdLBQbVWaxhGpVZr1GoNXJEs+2XZryhBWfaPjAQikTBeMk1LkkRQfxuwbRtERETOZprWnTt3vN4hvNRstg4O/hovHRxUTdPCayRJHBkJ4KWRkT/y+bx4qd1uHx+fDA563G436PYYsG0bRERE1IFpWjhDkkTQh2LAtm0QEREROZUAIiIiIgcTQERERORgAoiIiIgcTAARERGRgwkgIiIicjABRERERA4mgIiIiMjBBBARERE5mAAiIiIiBxNARERE5GACiIiIiBxMABEREZGDCSAiIiJyMAFEREREDiaAiIiIyMEEEBERETmYACIiIiIHE0BERETkYAKIiIiIHEwAERERkYMJICIiInIwAUREREQOJoCIiIjIwQQQEREROZgAIiIiIgcTQERERORgAoiIiIgcTAARERGRgwkgIiIicjABRERERA4mgIiIiMjBBBARERE5mAAiIiIiBxNARERE5GACiIiIiBxMABEREZGDCSAiIiJyMAFEREREDiaAiIiIyMEEEBERETmYACIiIiIHE0BERETkYAKIiIiIHEwAERERkYMJICIiInIwAUREREQOJoCIiIjIwQQQEREROZgAIiIiIgcTQERERORgAoiIiIgcTAARERGRgwkgIiIicjABRERERA4mgIiIiMjBBBARERE5mAAiIiIiBxNARERE5GACiIiIiBxMABEREZGDCSAiIiJyMAFEREREDiaAiIiIyMH+L23dJa8GW5DMAAAAAElFTkSuQmCC)

通常我们使用对象时，我们会把相关数据组合在一起。在这个例子，我们把夏洛克的姓和年龄组合到对象中。

```javascript
let sherlock = {
  surname: 'Holmes',
  age: 64,
};
```

这里sherlock还是一个变量，但是surname和age不是。它们是属性，和变量不同，属性属于特定的对象。

**在我们的Javascript宇宙中，属性和变量都像“电线”一样。**

我们的宇宙充满了电线，有的从变量指向值 有的从属性指向值，所有的电线都指向值。

```javascript
console.log(sherlock.age)
```

![图片](https://ci6.googleusercontent.com/proxy/8GVcnjJ5C7oqcExGIXhH8QAFVQo-h-s2frl_Y0o9bEGyLKFWuLgTjB6TCElKL9uLoO8hkdVQXcv_hPpFQiQk-VLiQd7eiSns82I2RXBqLljwvlj9W36b4xx0rSsfl1nodRsc90vgDbKDOK5MK0EuBPdlxPdbAqFT1gx4Bv_6ie2wjUqQPH0F=s0-d-e1-ft#https://res.cloudinary.com/dg3gyk0gu/image/upload/v1584416479/just-javascript-email-images/jj07/sherlock_readage.gif)

## 属性名

单个对象的属性名不重复，例如 sherlock 不会有2个属性 age。
属性名区分大小写，例如age和Age是不同的2个属性名。

## 分配给属性

```javascript
sherlock.age = 65
```

三部曲

找到左侧电线所指
![图片](https://ci6.googleusercontent.com/proxy/2ozJpC72LMy6fwAa6omMIF6Yj8upJ3thCmfOxDFJE-LqTBhIFIwO9Z5005_v6gKb1FvzhcyhU83QbxL8BT3MA4e7FYrsZCS3E5dMKXafBpVwQtq-fsuc2eHpC_Gbq4ALgM6-i56TAkVXnYTkO2FHIacPUEYmHCJm6lWVOe8txMs8hY26nhTFFnT6Ix5IMg=s0-d-e1-ft#https://res.cloudinary.com/dg3gyk0gu/image/upload/v1584416479/just-javascript-email-images/jj07/sherlock_reassign_age-1.gif)

在Javascript宇宙中召唤65
![图片](https://ci5.googleusercontent.com/proxy/u1-6f0N8LN5tGXX2LQU2etKehbCUFplROCqpi9INJvNGuNZTl25Fdqe1rXM0hIKISSmP4epzRpt4YHzUuahO-0DxlrH7gv0L6B9uYKonctf0RW42InO50jkg6fD-0j6jwfBVTmpkffTQlTUEyg3IRBtyYX9WhRvwyKkpFfg67n4PtK8X0crxCngcUNonOQ=s0-d-e1-ft#https://res.cloudinary.com/dg3gyk0gu/image/upload/v1584416480/just-javascript-email-images/jj07/sherlock_reassign_age-2.gif)

把左侧电线和右侧值连接
![tupian](https://ci6.googleusercontent.com/proxy/P4TXLPcSCXKDFEodEpKkiCt-grLi_fcQ50UzTttL5BR_qZrWYSKzgEwbNrxGO7htvlQFslhxCqgQGJC8Z--_PNkTAymfBnCYnpOzPiLqDv7npqhjyY-XDQGtvi0NJ_uHinKZzHlp3dNzW3QvoCQzkfqgTsBmCUbLiILOFZMCwnN7spdj-nASdWalMasSgw=s0-d-e1-ft#https://res.cloudinary.com/dg3gyk0gu/image/upload/v1584416479/just-javascript-email-images/jj07/sherlock_reassign_age-3.gif)

## 失踪属性

```javascript
let sherlock = { surname: 'Holmes', age: 64 };
console.log(sherlock.boat); // ?
```

查找规则

1. 找到.之前指向的值
2. 如果这个值是null或者是undefined，抛出错误
3. 检查这个属性是否存在：
   1. **存在**，返回这个属性指向的值
   2. **不存在**，返回undefined

```javascript
let sherlock = { surname: 'Holmes', age: 64 };
console.log(sherlock.boat.name); // ?
```

> sherlock有一个指向undefined的属性boat吗？

.

.

.

.

.

.

.

.

.

.

.

.

sherlock.boat.name 会抛出TypeError，是因为.boat是undefined，根据上面的查询规则，访问一个undefined值的属性抛出错误。

sherlock.boat不是 sherlock的属性，可以把这看作规则的一部分，而Javascript引擎遵守规则。
或者可以换一种理解，规则是当没有把值分配给属性这一步，当尝试获取一个对象指向的属性的值时，如果值不存在，则返回undefined。

```javascript
let sherlock = { surname: 'Holmes', age: 64, boat: undefined };
console.log(sherlock.boat); // ?
```

> boat是sherlock的属性吗？

## Q&A

## [Exercises](https://click.convertkit-mail.com/5qug8kxwzlh8ummm33t7/6qhehouddeqe27ho/aHR0cHM6Ly9lZ2doZWFkaW8udHlwZWZvcm0uY29tL3RvL0lESkJQUT9lbWFpbD1oLmxvdmUucHVyZUBnbWFpbC5jb20=)
