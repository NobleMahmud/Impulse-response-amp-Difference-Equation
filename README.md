# Impulse-response-amp-Difference-Equation

We have an arbitrary signal x ( n ) that we wish to resolve into a sum of unit
sample sequences. To utilize the notation estabiished in the preceding section. We select the
elementary signals xk (n) to be

where k represents the delay of the unit sample sequence. To handle an arbitrary signal x( n)
that may have nonzero values over an infinite duration. The set of unit impulses must also be
infinite. to encompass the infinite number of delays.
Now suppose that we multiply the two sequences x(n) and δ(n - k ) . Since δ(n - k ) is zero
everywhere except at n = k . where its value is unity. The result of this multiplication is
another sequence that is zero everywhere except at n = k, where its value is x ( k )

Matlab Code:
n = -12:1:12;
impulse=n == 0;
%subplot(1,2,1);
stem(n,impulse);
xlabel(&#39;n&#39;);
ylabel(&#39;\delta[n]&#39;);
title(&#39;Impulse Signal&#39;);
x = [1];
y = [1 -1/2];
y1=filter(x,y,impulse);
%subplot(1,2,2);
stem(n,y1);
xlabel(&#39;n&#39;);
ylabel(&#39;y[n]&#39;);
title(&#39;Impulse Response&#39;);
