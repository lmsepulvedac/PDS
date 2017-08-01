
# Sistemas de tiempo continuo LTI
***

Recordemos que en general, los sistemas se pueden clasificar como:

1.Causal y no causal:

>Un sistema es causal si su salida en un tiempo determinado solo depende de la entrada en el mismo instante de tiempo o en valor pasados:

>Si: $$y(t) = T[x(t)],$$

>donde $T[.]$ es el operador del sistema, entonces:

$$y(t) = T[x(t+t_0)]$$ 

>es un sistema no causal

2.Con memoria y sin memoria: 

>Un sistema se demonia sin memoria si su salida en un tiempo determinado depende de la entrada en ese  mismo instante de tiempo

3.Aditivo y no aditivo:

>Un sistema aditivo cumple que:

$$T[x_1(t)+x_2(t)]=T[x_1(t)+x_2(t)]=y_1(t)+y_2(t)$$

4.Homogéneo y no homogéneo:

>Para un sistema homogéneo se tiene que:

$$T[cx(t)]=cT[x(t)]=cy(t),$$

>donde $c$ es una constante

5.Lineal y no lineal:

>Para que un sistema sea lineal se debe cumplir que sea **homogéneo y aditivo**, esto es, que cumpla el principio de superposición.

$$T[\alpha x_1(t)+ \beta x_2(t)] = \alpha y_1(t)+ \beta y_2(t),$$

>con $\alpha$ y $\beta$ constantes.

6.Invariante y no invariante:

>En un sistema invariante en el tiempo un corrimiento en la entrada corresponde a un corrimiento en la salida.

$$T[x(t-\tau)]=y(t-\tau)$$

Un sistema LTI será por tanto un sistema lineal e invariante en el tiempo

## Respuesta al impulso de un sistema LTI de tiempo continuo

La respuesta al impulso LTI de tiempo continuo corresnde a la la salida de un sistema LTI cuando su entrada es un impulso, i.e. $x(t) = \delta$. En este orden, diremos que $y(t)=h(t)=T[x(t)]=T[\delta(t)]$.

En el caso de una entrada arbitraria diferente a un impulso, i.e. cualquier $x(t)$ que se pueda describir como
$x(t)=\int_{-\infty}^{\infty}x(\tau)\delta(t-\tau)d\tau$ por propiedades del $\delta(t)$, se tendra que:

$$y(t) = T[x(t)]=T\left[\int_{-\infty}^{\infty}x(\tau)\delta(t-\tau)d\tau\right]$$

Si el sistema es lineal, entonces:

$$y(t) = T\left[\int_{-\infty}^{\infty}x(\tau)\delta(t-\tau)d\tau\right] = \int_{-\infty}^{\infty}T[x(\tau)\delta(t-\tau)]d\tau$$

Si es invariante en el tiempo:

$$y(t) = \int_{-\infty}^{\infty}T[x(\tau)\delta(t-\tau)]d\tau =  \int_{-\infty}^{\infty}x(\tau)T[\delta(t-\tau)]d\tau$$

La expresión anterior será entonces:

$$y(t) = \int_{-\infty}^{\infty}x(\tau)T[\delta(t-\tau)]d\tau = \int_{-\infty}^{\infty}x(\tau)h(t-\tau)d\tau,$$

que es la definición de convolución continua. Por ello se puede establecer, que la respuesta al impulso $h(t)$ caracteriza un sistema LTI, y que dada esta función y cualquier entrada $x(t)$, se puede encontrar la salida del sistema.
