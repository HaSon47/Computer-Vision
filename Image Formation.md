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
