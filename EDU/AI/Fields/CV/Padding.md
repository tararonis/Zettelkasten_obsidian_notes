> пиксели по краям изображений имеют меньший вес, так как в них нельзя поставить центр свертки и соответсвенно к ним реже прикладывается фильтр

> чтобы этого избежать, к картинки дополняются пикселями так чтобы после свертки сохранился исходный размер изображения

## Zero-padding
![[Pasted image 20240613181138.png]]
> добавляем 0 на границах так чтобы посчитанная после этого свертка давала изображение того же размера как и исходное

> риск - сеть может научиться понимать где край изображения - какие-то фильтры обучатся на паттерны по краям картинок

## Reflection padding
![[Pasted image 20240613181354.png]]
> Край картинки отзеркаливается. Не получится находить края изображения, но теперь модель может начать находить зеркальные отражения и подбирать фильтры под них.

## Replication padding
![[Pasted image 20240613181514.png]]
>пиксель на границе равен ближайшему пикселю из изображения. Но тогда могут получиться какие-то константные области, на которые тоже может обучиться модель.


____
### Zero-Links

____
### Links
[[_CV]]