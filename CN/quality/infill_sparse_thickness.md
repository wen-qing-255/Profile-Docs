填充层厚度
====
### **Description**
启用此参数后，执行头将合并打印多层填充。多个填充层被合并起来后，打印头仅在这些填充层的最高层挤出耗材，通过过度挤出的方式，一次完成多个填充层的打印。

在分层视图中预览模型时，合并层的走线看起来比普通走线宽很多。但实际上，在打印这些较宽的填充走线时，耗材会向下延展，最终形成高度较大而非宽度较大的走线。

![Infill Layer Thickness is set to three times the layer height](../images/infill_sparse_thickness.png)

### **Usage**
由于填充的层高并不影响外观质量，因此可以使用较厚的填充层来节约打印时间。

合并的填充层厚度必须是原始层高的倍数。否则，填充层厚度将被四舍五入至最接近的层高数值。

* 请注意不要将填充层厚度设置过高。否则在模型的填充结构和其他结构之间切换时，喷嘴的材料流速就会出现大幅波动。挤出速率的增加和减少都有一定延迟，这会导致执行头在开始打印填充时挤出不足，而在填充打印结束后过度挤出。

* 在一定高度的打印部件中，若剩余高度小于合并的填充层厚度，则执行头会打印普通层高的薄打印层以填充剩余空间。这种做法在打印斜坡的时候尤其常见。打印斜坡时，由于执行头仅在合并层的最高层挤出耗材，即使耗材竖直向下延展，也无法填充到斜坡角。此时，执行头将会在剩余空间中打印高度较小的普通走线，来填充这些角落。