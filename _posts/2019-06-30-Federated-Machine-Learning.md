# 联邦机器学习

本文介绍联邦机器学习，这是机器学习领域正在探索的最新和最着名的方法之一，它侧重于利用分布式系统的力量来训练和增强机器学习模型。

随着IOT的出现和智能手机使用量的增加，具有数据的端点的数量呈指数增长。然而，传统的机器学习方法并不具备处理如此广泛分布的数据和训练模型的能力。

传统的机器学习方法包括用于存储数据和训练模型的中央服务器。然后有两种方法可以使用这种训练模型。

1.构建数据管道以使所有数据通过中央服务器，该服务器托管用于进行预测的训练模型。然后，通过仪表板共享预测结果或用于启动服务。该模型在行业中大量使用，以监控产品，提供建议和其他此类服务。该方法的缺点是由环境中存在的传感器/设备收集的所有输入将被发送回中央服务器，然后处理结果将被发回。这限制了模型根据环境快速学习和适应的能力，并提供实时结果。

2.第二种方法是将训练过的模型运送到直接在环境中相互作用的设备。随着硬件技术的改进，已经有可能具有足够的处理能力来运行这种预测模型。这种方法的好处是预测发生在收集输入的相同环境中并且更快。然而，即使在用于连续学习的该模型中，也要在每个设备处收集训练数据，然后将其发送回重新训练模型的服务器。

联邦机器学习是一种方法，它使我们能够通过在设备本身训练模型来摆脱这种复杂性。然后将这些经过训练的模型发送回中央服务器，在那里聚合它们（基本上调整它们的权重），然后将一个合并的模型发送回设备。它利用分布式计算的概念来维护设备上的每个模型的跟踪，在每个设备上聚合和重新分配模型。这种方法非常有利于在诸如手机，传感器等小型设备上运行低成本机器学习模型。它确实是开发更好和互联世界的门户。

### 联邦机器学习如何运作？

联邦机器学习大致采用以下简单步骤：

1.将预测模型发送到设备

2.消耗输入并进行预测。观察用户采取的行动并将差异存储为训练数据

3.使用此培训数据来改进预测模型。

4.将这些经过重新训练的模型从多个设备发送到中央服务器

5.从所有不同模型重新分配和聚合权重以创建一个模型

6.将重新训练的模型送回所有设备

这些步骤在循环中重复以实现连续学习的过程。

### 联邦机器学习的好处

联邦机器学习的一些主要好处是：

1. 数据安全和隐私：由于培训在设备上进行，只有模型被运回，因此摆脱了在黑客攻击的中心位置存储大量高度敏感或个人数据的主要问题之一。

2. 实时预测：由于预测发生在设备本身，这种方法也消除了由于将输入传输回中央服务器然后将结果发送回设备而发生的时间延迟

3. 离线预测：由于模型存在于设备上，即使没有可用的互联网连接，预测仍然有效。只要设备能够获得输入，就可以利用预测模型来完成他们的工作。

4. 最小的基础设施：这种方法需要最少的硬件（我们的移动设备中可用的硬件绰绰有余）来运行机器学习模型，并真正实现机器学习的强大功能。

### 使用联邦机器学习

这种方法很新，但它的使用虽然有限，但已经出现在一些关键的地方。Google键盘是使用此方法的主要示例之一。该技术非常强大，并且还有许多其他用例，可以利用它们，例如工业矿山，大型农场，沙漠，确保连续的互联网连接是基础设施和成本方面的挑战。

### 挑战

一些主要挑战是：

1.维护大规模分布式系统

2.始终与所有设备的连接有限

3.偏差或反馈方面的数据不平衡。然而，通过巧妙地选择在给定时刻从其获得反馈的设备，可以将该问题有效地减少

4.开发能够跟上方法所涉及的动态和持续学习的基础设施或模型

5.跨高度分布的数据集运行优化算法

### 未来的步骤

目前，模型在设备上受到训练，并且使用本地数据进行了改进。下一个明显的步骤是开发一种跨设备训练模型的能力，以便每个模型可以从所有附近的设备中学习。这仍然是未来，但我们只能想象一旦开发这种方法，机器学习可以产生的效率和实用性。