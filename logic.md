# Logic

Mệnh đề là một phát biểu có thể đúng hoặc sai, nhưng không thể vừa đúng vừa sai.


| Ký hiệu               | Ý nghĩa                              |
| :-------------------- | :----------------------------------- |
| ${\sim} P$            | Phủ định của $P$                     |
| $P \vee Q$            | $P$ hoặc $Q$                         |
| $P \wedge Q$          | $P$ và $Q$                           |
| $P \oplus Q$          | Hoặc $P$ hoặc $Q$, không phải cả hai |
| $P \Rightarrow Q$     | Nếu $P$ thì $Q$                      |
| $P \Leftrightarrow Q$ | $P$ khi và chỉ khi $Q$               |



Dạng mệnh đề (propositional form) là các mệnh đề phức được tạo thành bằng cách kết hợp các biến mệnh đề thông qua toán tử logic. Ví dụ:
$$
  (P \wedge ({\sim} Q)) \vee (({\sim} P) \wedge Q)
$$

## Mệnh đề tương đương
Hai dạng mệnh đề $A$ và $B$ được gọi là tương đương về mặt logic nếu bảng giá trị logic của chúng giống nhau ở mọi dòng. Khi đó, ta ký hiệu $A \equiv B$. Ngược lại, nếu $A$ và $B$ không tương đương, ta ký hiệu $A \not\equiv B$.

Định lý về mệnh đề tương đương: Với các mệnh đề $P, Q$ và $R$ bất kỳ, ta luôn có

1. Giao hoán: 
$$
  \begin{aligned}
    P \wedge Q &\equiv Q \wedge P\\
    P \vee Q &\equiv Q \vee P \\
    P \oplus Q &\equiv Q \oplus P.
  \end{aligned}
$$
2. Kết hợp: 
$$
 \begin{aligned}
   P \wedge (Q \wedge R) &\equiv (P \wedge Q) \wedge R \\ 
   P \vee (Q \vee R) &\equiv (P \vee Q) \vee R\\ 
   P \oplus (Q \oplus R) &\equiv (P \oplus Q) \oplus R.
 \end{aligned} 
$$
3. Phân phối: 
$$
 \begin{aligned}
   P \wedge (Q \vee R) &\equiv (P \wedge Q) \vee (P \wedge R) \\ 
   P \vee (Q \wedge R) &\equiv (P \vee Q) \wedge (P \vee R) \\ 
   P \wedge (Q \oplus R) &\equiv (P \wedge Q) \oplus (P \wedge R)
 \end{aligned} 
$$
4. Luỹ đẳng: $P \wedge P \equiv P$, và $P \vee P \equiv P$.
5. Hấp thụ: $P \wedge (P \vee Q) \equiv P$, và $P \vee (P \wedge Q) \equiv P$.
6. Phủ định: 
$$
 \begin{aligned}
   {\sim} ({\sim} P) &\equiv P \\ 
   {\sim} (P \wedge Q) &\equiv ({\sim} P) \vee ({\sim} Q) \\ 
   {\sim} (P \vee Q) &\equiv ({\sim} P) \wedge ({\sim} Q).
 \end{aligned} 
$$

## Mệnh đề kéo theo
Mệnh đề có dạng "Nếu $P$ thì $Q$" được gọi là một mệnh đề kéo theo. Trong đó, $P$ được gọi là *giả thiết* và $Q$ là *kết luận*.

Với hai mệnh đề $P, Q$ bất kỳ, bảng giá trị logic của $P \Rightarrow Q$ được xác định như sau:

|  $P$  |  $Q$  | $P \Rightarrow Q$ |
| :---: | :---: | :---------------: |
|   T   |   T   |         T         |
|   T   |   F   |         F         |
|   F   |   T   |         T         |
|   F   |   F   |         T         |

Chú ý rằng $P \Rightarrow Q$ chỉ sai trong trường hợp giả thiết $P$ đúng và kết luận $Q$ sai.

Định lý. Cho $P$ và $Q$ là hai mệnh đề phân biệt, khi đó:

1. $P \Rightarrow Q \quad  \not \equiv \quad Q \Rightarrow P$.
2. $P \Rightarrow Q \quad \equiv \quad  ({\sim} Q) \Rightarrow ({\sim} P)$.
3. $P \Rightarrow Q \quad \equiv \quad ({\sim} P) \vee Q$.
4. ${\sim} (P \Rightarrow Q) \equiv P \wedge ({\sim} Q)$.

## Bài tập {.unnumbered}
**Bài 1**. Lập bảng giá trị logic của mỗi dạng mệnh đề sau\
a) $(P \vee \overline{Q}) \Rightarrow P$ \
b) $P \Rightarrow (Q \wedge \overline{P} )$\
c) $(P \oplus Q) \Rightarrow (P \vee Q)$

**Bài 2**. Lập bảng giá trị logic của mỗi dạng mệnh đề sau \
a) $(P \Rightarrow Q) \wedge (Q\Rightarrow R)$ \
b) $(P \Rightarrow Q) \Rightarrow (Q \vee R)$ \
c) $({\sim} (P \oplus Q)) \Rightarrow ({\sim} (R \wedge P))$

**Bài 3**. Chứng minh luật phủ định ${\sim} ({\sim} P) \equiv P$ và ${\sim} (P \wedge Q) \equiv ({\sim}P) \vee ({\sim} Q)$ bằng bảng giá trị logic.

**Bài 4**. Chứng minh tính chất kết hợp đối với $\wedge$ và $\vee$.

**Bài 5**. Chứng minh tính chứng phân phối trong định lý về mệnh đề tương đương.

**Bài 6**. Khẳng định sau đúng hay sai? Tại sao?
$$
  ({\sim}P)\oplus (Q \oplus P) \equiv ({\sim}Q)
$$


