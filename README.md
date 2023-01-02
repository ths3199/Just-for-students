# Trade-Profit-Calculator
...
print("비교우위를 이용한 무역이고, 무역의 교환비는 1:1입니다")

a1, a11, a2, a22 = input("A국의 생산품의 이름과 생산비용을 띄어쓰기로 구분하여 차례대로 입력하세요.(예시:신발 50 모자 40): ").split()
b1, b11, b2, b22 = input("앞에서와 같이 B국의 생산품의 이름과 생산비용을 띄어쓰기로 구분하여 차례대로 입력하세요. 생산품의 이름과 입력순서는 앞과 같아야합니다.:").split()

Aa1_oc = int(a11)/int(a22)
Aa2_oc = int(a22)/int(a11)
Bb1_oc = int(b11)/int(b22)
Bb2_oc = int(b22)/int(b11)

if Aa1_oc > Aa2_oc:
  Aca = a22
elif Aa1_oc == Aa2_oc:
  Aca = a11
else:
  Aca = a11
if Bb1_oc > Bb2_oc:
  Bca = b22
elif Bb1_oc == Bb2_oc:
  Bca = b11
else:
  Bca = b11

Aocost = int(a11) + int(a22)
Accost = int(Aca) + int(Aca)
Bocost = int(b11) + int(b22)
Bccost = int(Bca) + int(Bca)


Ata = Aocost - Accost
Bta = Bocost - Bccost
print("/n비교우위를 이용해 무역을 하면 A는 {}만큼 이득, B는 {}만큼 이득입니다.".format(Ata, Bta))
