# Image Formation

#### Homogeneous Coordinate

`Đề cập đến khái niệm tọa độ homogeneous`

Xét trong tọa độ 2D decac, mỗi point x được biểu diễn: $\mathbf{x}=(x,y)$.

> Khi đó các phép biến đổi như xoay, scale được biểu diễn bởi:
> 
> $$
> \mathbf{x'} = \mathbf{M}\mathbf{x}
> $$

> Phép tịnh tiến:
> 
> $$
> \mathbf{x'}=\mathbf{x}+ \mathbf{v}
> $$

> Btw, ta muốn biểu diễn cả phép tịnh tiến thông qua ma trận

Khi đó, xét homogeneous coordinate 

> Mỗi point 2D được biểu diễn bởi: $\tilde{\mathbf{x}}=(\tilde{x},\tilde{y},\tilde{w}) \in P^3 (= R^3 \setminus (0,0,0))$
> 
> Trong đó, các điểm có cùng tỉ lệ sẽ được coi là tương đương nhau:
> 
> $$
> \tilde{\mathbf{x}} = \tilde{\mathbf{w}}(x,y,1)
=\tilde{\mathbf{w}}.\bar{\mathbf{x}}
> $$

> và cùng tương đương với $\bar{\mathbf{x}}=(x,y,1)$ $\rightarrow$ augmented vector của $\mathbf{x}$ trong tọa độ decac

> Khi đó, mọi phép biến đổi bao gồm tịnh tiến đều được biểu diễn qua:
> 
> $$
> \tilde{\mathbf{x}}' = \mathbf{M}\tilde{\mathbf{x}}
> $$

#### Quaternion:

`Tập hợp mở rộng của Complex, kí hiệu` $\mathbf{H}$

> $q= a+bi+cj+dk$
> 
> trong đó:
> 
> $a,b,c,d \in R$
> 
> $i,j,k$ là đơn vị ảo thỏa mãn: $i^2=j^2=k^2=ijk=-1$

> Thường dùng để biểu diễn phép rotation.

Unit quaternions:

> $\mathbf{q}\in\mathbf{H}: ||\mathbf{q}||=1$

## Geometric primitives

`Các cách để biểu diễn điểm, đường thẳng, mặt phẳng 2D 3D trong Geometric` 

### 2D

**Point**

> $\mathbf{x}=(x,y) \in  R^2$

> $\tilde{\mathbf{x}} = (\tilde{x},\tilde{y},\tilde{w}) \in P^3$

Điểm $(x,y,0)$: ideal points

**Line**

> $\tilde{\mathbf{l}}=(a,b,c)$ 
> 
> Line equation:
> 
> $$
> \bar{\mathbf{x}}\tilde{\mathbf{l}} = ax+by+c=0
> $$

Chuẩn hóa

> $\tilde{\mathbf{l}} = (\hat{n_x},\hat{n_y},d)$ $=(\hat{\mathbf{n}},d)$
> 
> Trong đó: 
> 
> $\hat{\mathbf{n}}$ là vecto pháp tuyến $||\hat{\mathbf{n}}||=1$
> 
> $d$ là khoảng cách đến tâm O

Polar coordinates

> $\hat{\mathbf{n}} = (\cos \theta, \sin \theta)$ $\rightarrow \tilde{\mathbf{l}}= (\theta,d)$

- Line at infinity: $\tilde{\mathbf{l}} =(0,0,1)$ : include all ideal points

- Intersection of two lines: 
  
  $$
  \tilde{\mathbf{x}} = \tilde{\mathbf{l_1}}\times \tilde{\mathbf{l_2}}
  $$
  
  > Trong đó $\times$ là cross product.
  > 
  > Cụ thể: vì $\tilde{\mathbf{x}}$ thuộc $\tilde{\mathbf{l_1}}$ và $\tilde{\mathbf{l_2}}$ nên $\tilde{\mathbf{x}}.\tilde{\mathbf{l_1}}=0$ và $\tilde{\mathbf{x}}.\tilde{\mathbf{l_2}}=0$

- Joining 2 points:
  
  $$
  \tilde{\mathbf{l}} = \tilde{\mathbf{x_1}} \times
\tilde{\mathbf{x_2}}
  $$

### 3D

**Points** 

> $\mathbf{x} = (x,y,z) \in R^3$

Homogeneous Coordinate

> $\tilde{\mathbf{x}}=(\tilde{x},\tilde{y},\tilde{z},\tilde{w})$

**Planes**

> $\tilde{\mathbf{m}}=(a,b,c,d)$.
> 
> Plane equation:
> 
> $$
> \tilde{\mathbf{x}}.\tilde{\mathbf{m}}= 
ax+by+cz+d=0
> $$

> $\tilde{\mathbf{m}}=(\hat{n_x},\hat{n_y},\hat{n_y},d)$ $=(\hat{\mathbf{n}},d)$
> 
> Trong đó:
> 
> $\hat{\mathbf{n}}$ là vecto pháp tuyến $||\hat{\mathbf{n}}||=1$
> 
> d là khoảng cách đến tâm O

Spherical coordinates

> $\hat{\mathbf{n}} \rightarrow \theta, \phi$ : $\hat{\mathbf{n}} = (\cos \theta \cos\phi, \sin\theta\cos\phi, \sin\phi)$
> 
> $\rightarrow \tilde{\mathbf{m}}= (\theta, \phi,d)$

## Geometric Transformation

`Các cách biểu diễn các phép biến đổi 2D, 3D trong Geometric`

note: 

$\mathbf{x}:$ tọa độ decac

$\bar{\mathbf{x}}:$ augment vector

$\tilde{\mathbf{x}}:$ homogeneous coordinate

#### 2D

![](C:\Users\Lenovo\OneDrive%20-%20Hanoi%20University%20of%20Science%20and%20Technology\Desktop\Self_learning\Computer-Vision\image\2Dtrans.png)

> where $\mathbf{R}$ is an orthonormal matrix $\mathbf{RR}^T= \mathbf{I}$ and $\det(\mathbf{R})=1$
> 
> $$
> R = \begin{bmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta 
\end{bmatrix} 
> $$

#### 3D

![](C:\Users\Lenovo\OneDrive%20-%20Hanoi%20University%20of%20Science%20and%20Technology\Desktop\Self_learning\Computer-Vision\image\3Dtrans.png)

Represent rotation : parameterizing $\mathbf{R}$:

1. Euler angles
   
   > $\mathbf{R}$ : product of three rotations around three cardinal axes: $\alpha, \beta, \gamma$
   
   > note: nhiều khả năng gặp Gimbal lock

2. Axis-Angle (Exponential Twist)
   
   > $(\hat{\mathbf{n}}, \theta)$ 
   > 
   > where $\hat{\mathbf{n}}=(\hat{n}_x,\hat{n}_y,\hat{n}_z)$ is trục quay, $\theta$ is góc quay. 
   > 
   > We have Rodrigues's formula:
   > 
   > $$
   > \mathbf{R}(\hat{\mathbf{n}},\theta)=
\mathbf{I}+\sin\theta[\hat{\mathbf{n}}]_{\times}
+(1-\cos\theta)[\hat{\mathbf{n}}]_{\times}^2
   > $$
   > 
   > where
   > 
   > $$
   > [\hat{\mathbf{n}}]_{\times}=
\begin{bmatrix}
0 & -\hat{n}_z & \hat{n}_y \\
\hat{n}_z & 0 & -\hat{n}_x \\
-\hat{n}_y & \hat{n}_x & 0
\end{bmatrix}
   > $$

3. Unit quaternions
   
   > $\mathbf{q}=(\mathbf{v},w)=(\sin \frac{\theta}{2}\hat{\mathbf{n}},\cos \frac{\theta}{2})$
   > 
   > where $\hat{\mathbf{n}}, \theta$ are the rotation axis and angle
   > 
   > We have:
   > 
   > $$
   > \mathbf{R}(\hat{\mathbf{n}},\theta)=
\mathbf{I}+2w[\mathbf{v}]_{\times}
+2[\mathbf{v}]_{\times}^2
   > $$
   > 
   > or with unit quaternion $\mathbf{q}=(x,y,z,w):$
   > 
   > $$
   > \mathbf{R}(\mathbf{q})=
\begin{bmatrix}
1-2(y^2+z^2)&2(xy-zw)&2(xz+yw)\\
2(xy+zw)&1-2(x^2+z^2)&2(yz-xw)\\
2(xz-yw)&2(yz+xw)&1-2(x^2+y^2)
\end{bmatrix}
   > $$
   > 
   >  .
   
   > Dùng cái này thì dễ để biểu diễn nhân các phép quay hay là lấy inverse
   
   Quaternion multiply operator:
   
   > $\mathbf{q}_0=(\mathbf{v}_0,w_0)$ , $\mathbf{q}_1=(\mathbf{v}_1,w_1)$
   
   > $\mathbf{q}_2=\mathbf{q}_0\mathbf{q}_1=(\mathbf{v}_0\times\mathbf{v}_1+w_0\mathbf{v}_1+w_1\mathbf{v}_0,w_0w_1-\mathbf{v}_0\mathbf{v}_1)$
   > 
   > we have:
   > 
   > $$
   > \mathbf{R}(\mathbf{q}_2)=
\mathbf{R}(\mathbf{q}_0)
\mathbf{R}(\mathbf{q}_1)
   > $$
   
   Inverse of a quaternion:
   
   > Just flip the sign of $\mathbf{v}$ or $w$ $=$ lấy transposing của $\mathbf{R}$
   
   Quaternion division:
   
   > $\mathbf{q}_2=\mathbf{q}_0/\mathbf{q}_1=\mathbf{q}_0\mathbf{q}_1^{-1}=(\mathbf{v}_0\times\mathbf{v}_1+w_0\mathbf{v}_1-w_1\mathbf{v}_0,-w_0w_1-\mathbf{v}_0\mathbf{v}_1)$

#### 3D to 2D projections
