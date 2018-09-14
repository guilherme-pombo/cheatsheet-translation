**1. Aprendizagem Supervisionada**

&#10230;

<br>

**2. Introdução a aprendizagem Supervisionada**

&#10230;

<br>

**3. Tendo um conjunto de pontos {x(1),...,x(m)} e as respectivas observações (ou classificações) associadas {y(1),...,y(m)}, nós queremos construir um modelo que aprenda a prever {y} tendo em conta {x}**

&#10230;

<br>

**4. Tipos de predição ― Os diferentes tipos de modelos preditivos estão sumarisados na tabela em baixo:**

&#10230;

<br>

**5. [Regressão, Classificação, Resultado, Exemplos]**

&#10230;

<br>

**6. [Contínuo, Classe, Regressão linear, Regressão logística, SVM, Naive Bayes]**

&#10230;

<br>

**7. Tipos de modelo ― Os diferentes tipos de modelo estaão sumarisadas na tabela em baixo:**

&#10230;

<br>

**8. [Modelo discriminativo, Modelo generativo, Objectivo, O que o modelo aprende, Ilustração, Exemplos]**

&#10230;

<br>

**9. [Estimar P(y|x) directamente, Estimar P(x|y) para depois deduzir P(y|x), Linha de decisão, Distribuições probabilísticas da data, Regressões, SVMs, GDA, Naive Bayes]**

&#10230;

<br>

**10. Notações e conceitos gerais**

&#10230;

<br>

**11. Hipótese ― A hipótese é denotada hθ e é o modelo que nós escolhemos para resolver o problema. Para um ponto x(i) a predição do modelo é denotada hθ(x(i)).**

&#10230;

<br>

**12. Função perda ― Uma Função perda é um função L:(z,y)∈R×Y⟼L(z,y)∈R que calcula quão diferentes a predição do modelo, {z}, e o verdadeiro valor, {y}, são. As funções de perda mais comuns estão sumarisadas na tabela em baixo:**

&#10230;

<br>

**13. [Erro dos quadrados mínimos, Perca logística, Perca dobradiça?, Entropia Cruzada]**

&#10230;

<br>

**14. [Regressão linear, Regressão logística, SVM, Redes neuronais]**

&#10230;

<br>

**15. Função de custo ― A função de custo J é geralmente usada para avaliar o desempenho do modelo, e é definida usando a função de perca L da seguinte maneira:**

&#10230;

<br>

**16. Método do gradiente ― Denotamos α∈R a velocidade de aprendizagem, o método do gradiente é actualizado a cada passo usando a função de perca J da seguinte maneira:**

&#10230;

<br>

**17. Observação: Método do gradiente estocástico (SGD) faz o passo de aprendizagem para cada dado de treino individual, e o método do gradiente estocástico com mini-lote executa o passo de aprendizagem num conjunto de dados.**

&#10230;

<br>

**18. Verossimilhança ― A verossimilhança de um modelo L(θ) tendo em conta parâmetros θ é usada para encontrar os parâmetros do modelo mais correctos θ através de maximizar a verossimilhança. Na prática nós usamos o logaritmo da verossimilhança ℓ(θ)=log(L(θ)) visto que é mais fácil de optimisar:**

&#10230;

<br>

**19. Algoritmo de Newton ― O algoritmo de Newton é um método numérico que encontra θ de maneira que ℓ′(θ)=0. A regra para actualizar os parâmetros é:**

&#10230;

<br>

**20. Observação: a generalização para múltiplas dimensões, chamado Newton-Raphson method, actualiza os parâmetros da seguinte maneira:**

&#10230;

<br>

**21. Modelos lineares**

&#10230;

<br>

**22. Regressão linear**

&#10230;

<br>

**23. Assuma que y|x;θ∼N(μ,σ2)**

&#10230;

<br>

**24. Sistema de equações ― Usemos X para representar a matriz com {m} linhas, em que cada linha contém um vetor {x_i}, o valor de θ que minimiza a função de custo, é dado pela equação seguinte:**

&#10230;

<br>

**25. Algoritmo LMS ― Usemos α para representar a velocidade de aprendizagem, o algoritmo dos Quadrados Mínimos (LMS em inglês), também conhecido como regra de Widrow-Hoff, para dados de treino com {m} pontos, é dado pela seguinte equação:**

&#10230;

<br>

**26. Note: Esta equação é uma variação do método de gradiente.**

&#10230;

<br>

# TODO: dunno how to translate this properly
**27. LWR ― Regressão ponderada localmente (LWR em inglês) é uma variação que pesa cada ponto do conjunto de treino in its cost function by w(i)(x), which is defined with parameter τ∈R as:**

&#10230;

<br>

**28. Classificação e regressão logística**

&#10230;

<br>

**29. Função sigmóide ― A função sigmóide g, também conhecida como função logística, é definida da seguinte maneira:**

&#10230;

<br>

**30. Regressão logística ― Assumindo que y|x;θ∼Bernoulli(ϕ). Apresentamos o problema de regressão da seguinte maneira:**

&#10230;

<br>

**31. Note: Não existe solução fixa para regressão logística. A solução tem de ser sempre achada de maneira iterativa**

&#10230;

<br>

**32. Regressão Softmax ― A regressão softmax, também conhecida como regressão logística para multíplas classes, é usada para generalisar a regressão logística para casos com mais de 2 classes. Por convenção usamos θK=0, que faz com que o parâmetro de Bernoulli ϕi para cada classe {i} igual a:**

&#10230;

<br>

**33. Modelos lineares generalisados**

&#10230;

<br>

# TODO: dunno
**34. Familía exponencial ― Uma distribuição é exponencial if it can be written in terms of a natural parameter, also called the canonical parameter or link function, η, a sufficient statistic T(y) and a log-partition function a(η) as follows:**

&#10230;

<br>

**35. Remark: we will often have T(y)=y. Also, exp(−a(η)) can be seen as a normalization parameter that will make sure that the probabilities sum to one.**

&#10230;

<br>

**36. As distribuições exponenciais mais comuns estão sumarisadas na tabela seguinte:**

&#10230;

<br>

**37. [Distribuição, Bernoulli, Gaussiana, Poisson, Geométrica]**

&#10230;

<br>

**38. Suposições de modelos lineares generalisados ― Este tipo de modelos tem como objectivo prever a variável aleatória {y} como função de x∈Rn+1 e fazem as seguintes suposições:**

&#10230;

<br>

**39. Note: O algoritmo dos quadrados mínimos e regressão logística sao casos especiais de Modelos lineares generalisados.**

&#10230;

<br>

**40. Máquina de vetores de suporte**

&#10230;

<br>

**41: O objectivo das máquinas de vetores de suporte (SVM em inglês) é encontrar a função que separa as classes de maneira que os exemplos de cada categoria sejam divididos por um espaço claro que seja tão amplo quanto possível.**

&#10230;

<br>

**42: Optimal margin classifier ― The optimal margin classifier h is such that:**

&#10230;

<br>

**43: where (w,b)∈Rn×R is the solution of the following optimization problem:**

&#10230;

<br>

**44. such that**

&#10230;

<br>

**45. support vectors**

&#10230;

<br>

**46. Remark: the line is defined as wTx−b=0.**

&#10230;

<br>

**47. Hinge loss ― The hinge loss is used in the setting of SVMs and is defined as follows:**

&#10230;

<br>

**48. Kernel ― Given a feature mapping ϕ, we define the kernel K to be defined as:**

&#10230;

<br>

**49. In practice, the kernel K defined by K(x,z)=exp(−||x−z||22σ2) is called the Gaussian kernel and is commonly used.**

&#10230;

<br>

**50. [Non-linear separability, Use of a kernel mapping, Decision boundary in the original space]**

&#10230;

<br>

**51. Remark: we say that we use the "kernel trick" to compute the cost function using the kernel because we actually don't need to know the explicit mapping ϕ, which is often very complicated. Instead, only the values K(x,z) are needed.**

&#10230;

<br>

**52. Lagrangian ― We define the Lagrangian L(w,b) as follows:**

&#10230;

<br>

**53. Remark: the coefficients βi are called the Lagrange multipliers.**

&#10230;

<br>

**54. Generative Learning**

&#10230;

<br>

**55. A generative model first tries to learn how the data is generated by estimating P(x|y), which we can then use to estimate P(y|x) by using Bayes' rule.**

&#10230;

<br>

**56. Gaussian Discriminant Analysis**

&#10230;

<br>

**57. Setting ― The Gaussian Discriminant Analysis assumes that y and x|y=0 and x|y=1 are such that:**

&#10230;

<br>

**58. Estimation ― The following table sums up the estimates that we find when maximizing the likelihood:**

&#10230;

<br>

**59. Naive Bayes**

&#10230;

<br>

**60. Assumption ― The Naive Bayes model supposes that the features of each data point are all independent:**

&#10230;

<br>

**61. Solutions ― Maximizing the log-likelihood gives the following solutions, with k∈{0,1},l∈[[1,L]]**

&#10230;

<br>

**62. Remark: Naive Bayes is widely used for text classification and spam detection.**

&#10230;

<br>

**63. Tree-based and ensemble methods**

&#10230;

<br>

**64. These methods can be used for both regression and classification problems.**

&#10230;

<br>

**65. CART ― Classification and Regression Trees (CART), commonly known as decision trees, can be represented as binary trees. They have the advantage to be very interpretable.**

&#10230;

<br>

**66. Random forest ― It is a tree-based technique that uses a high number of decision trees built out of randomly selected sets of features. Contrary to the simple decision tree, it is highly uninterpretable but its generally good performance makes it a popular algorithm.**

&#10230;

<br>

**67. Remark: random forests are a type of ensemble methods.**

&#10230;

<br>

**68. Boosting ― The idea of boosting methods is to combine several weak learners to form a stronger one. The main ones are summed up in the table below:**

&#10230;

<br>

**69. [Adaptive boosting, Gradient boosting]**

&#10230;

<br>

**70. High weights are put on errors to improve at the next boosting step**

&#10230;

<br>

**71. Weak learners trained on remaining errors**

&#10230;

<br>

**72. Other non-parametric approaches**

&#10230;

<br>

**73. k-nearest neighbors ― The k-nearest neighbors algorithm, commonly known as k-NN, is a non-parametric approach where the response of a data point is determined by the nature of its k neighbors from the training set. It can be used in both classification and regression settings.**

&#10230;

<br>

**74. Remark: The higher the parameter k, the higher the bias, and the lower the parameter k, the higher the variance.**

&#10230;

<br>

**75. Learning Theory**

&#10230;

<br>

**76. Union bound ― Let A1,...,Ak be k events. We have:**

&#10230;

<br>

**77. Hoeffding inequality ― Let Z1,..,Zm be m iid variables drawn from a Bernoulli distribution of parameter ϕ. Let ˆϕ be their sample mean and γ>0 fixed. We have:**

&#10230;

<br>

**78. Remark: this inequality is also known as the Chernoff bound.**

&#10230;

<br>

**79. Training error ― For a given classifier h, we define the training error ˆϵ(h), also known as the empirical risk or empirical error, to be as follows:**

&#10230;

<br>

**80. Probably Approximately Correct (PAC) ― PAC is a framework under which numerous results on learning theory were proved, and has the following set of assumptions: **

&#10230;

<br>

**81: the training and testing sets follow the same distribution **

&#10230;

<br>

**82. the training examples are drawn independently**

&#10230;

<br>

**83. Shattering ― Given a set S={x(1),...,x(d)}, and a set of classifiers H, we say that H shatters S if for any set of labels {y(1),...,y(d)}, we have:**

&#10230;

<br>

**84. Upper bound theorem ― Let H be a finite hypothesis class such that |H|=k and let δ and the sample size m be fixed. Then, with probability of at least 1−δ, we have:**

&#10230;

<br>

**85. VC dimension ― The Vapnik-Chervonenkis (VC) dimension of a given infinite hypothesis class H, noted VC(H) is the size of the largest set that is shattered by H.**

&#10230;

<br>

**86. Remark: the VC dimension of H={set of linear classifiers in 2 dimensions} is 3.**

&#10230;

<br>

**87. Theorem (Vapnik) ― Let H be given, with VC(H)=d and m the number of training examples. With probability at least 1−δ, we have:**

&#10230;
