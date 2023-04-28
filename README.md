# Phys
In the nt coordinate system, does the normal acceleration depend only on the tangential velocity? Or in the case we also have a normal velocity in play, does the normal velocity also affect it?

[![enter image description here][1]][1]


When looking at the definition of the normal component (an) of acceleration, it seems like it depends on the magnitude squared of the velocity, meaning the normal velocity would also affect it:

$$a_{n} = \frac{(\sqrt{v_{t}²+v_{n}²})^2}ρ$$

However, when looking at this specific problem:
[![enter image description here][2]][2]


  [1]: https://i.stack.imgur.com/PDd4n.png
  [2]: https://i.stack.imgur.com/9CpRl.png

For the case I am trying to make, let us assume that at t = 0 we already have
$$v_{n} = 0.5 \frac{m}s$$
$$v_{to}=3\frac{m}{s}$$

We can use angular momentum to calculate the final tangential velocity, which ends up being
$$v_{tf} = \frac{8}{6}v_{to}=4\frac{m}{s}$$

Now to calculate the work done in the system we can use the final and initial states, having
$$U=\frac{1}{2}mv_{f}^{2}-\frac{1}{2}mv_{o}^{2}$$
$$U=\frac{1}{2}m\left(\sqrt{v_{tf}^{2}+v_{n}^{2}}\right)^{2}-\frac{1}{2}m\left(\sqrt{v_{to}^{2}+v_{n}^{2}}\right)^{2}$$
$$U=\frac{1}{2}200\left(\sqrt{\left(\frac{8}{6}3\right)^{2}+0.5^{2}}\right)^{2}-\frac{1}{2}200\left(\sqrt{3^{2}+0.5^{2}}\right)^{2}=700\ J$$

Now, if we wanted to calculate the work using the formal definition:
$$U=\int_{s_{1}}^{s_{2}}Fds$$

We can modify it into:
$$U=\int_{t_{1}}^{t_{2}}F\cdot\frac{ds}{dt}dt$$

Where ds is in the direction of the force (tension of cable), normal
$$U=\int_{t_{1}}^{t_{2}}ma_{n}\cdot v_{n}dt$$
$$U=\int_{0}^{4}m\left(\frac{v\left(t\right)^{2}}{ρ\left(t\right)}\right)\cdot v_{n}dt$$

We know:
$$ρ\left(t\right)=8-0.5t$$

And I would assume that this v(t) would be (following our first statement about normal acceleration), the magnitude of the velocity:
$$v\left(t\right)=\sqrt{v_{t}\left(t\right)^{2}+v_{n}^{2}}$$

However, when I plug this into Desmos, I only get U=700 J when this velocity is the tangential velocity:
$$v_{t}\left(t\right)$$

Thus:
$$U=\int_{0}^{4}m\left(\frac{v_{t}\left(t\right)^{2}}{p\left(t\right)}\right)\cdot v_{n}dt=700\ J$$

This seems to contradict the first statement that the normal acceleration depends on the magnitude squared of the velocity. I was wondering what is the problem then? Did I miss something in my calculation of work, or the normal acceleration only depends on Tangential velocity?
