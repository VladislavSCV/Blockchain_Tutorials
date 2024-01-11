# Blockchain
- В общем и целом представляет из себя особую базу данных. Под особой я имел ввиду ряд факторов присущих блокчейну.
  Факторы:
1) Блокчейн - децентрализованное место хранения данных
2) В блокчейне все имеют равные права
3) Блокчейн обеспечивает прозрачность транзакций: каждая транзакция записывается и может быть просмотрена любым участником сети.
4) Блокчейн обладает высокой степенью безопасности: благодаря криптографическим методам, данные в блокчейне практически невозможно подделать или изменить.
5) Блокчейн обеспечивает непрерывность и неизменность данных: каждый новый блок содержит информацию о предыдущем, формируя таким образом непрерывную цепочку.
6) Блокчейн позволяет совершать транзакции без посредников, что упрощает процесс и снижает стоимость транзакций.

Если переводить слово Blockchain дословно, то будет очевидно, что Block переводиться как блок!!! Ну а chain как цепь. Следовательно Blockchain есть цепочка из 
блоков. 

Вот норм фото, чтобы лучше понять)))
https://www.ipfa.org/wp-content/uploads/2022/09/Blockchain-Digitalisation-Image-scaled.jpeg

Предлагаю разобрать, что находится в этом блоке?!?!?!?
Окей, я сразу начну показывать примеры кода на go, чтобы реально было понять 'эти ваши блоки'

```
type Block struct {
	PrevBlockHash []byte
	Data          []byte
	Hash          []byte
	Timestamp     int64
	Nonce         int
}
```

Супер, тут мы создаем сам блок, а точнее его структуру. 
Соответственно, можно понять, что блок имеет важные состовляющие: 
- Хеш предыдущего блока
- Данные которые будут храниться в блоке
- Хэш блока
- Время создания блока
- это счетчик. (на самом деле сам забыл как называется это, если найдешь благоразумное название, то... сбрось пж)

Ну а blockchain соответсвено просто массив из блоков

```
type Blockchain struct {
	blocks []*Block
}
```

#ТУТОРИАЛЫ
1) https://habr.com/ru/articles/348672/
2) https://github.com/hlongvu/blockchain-go-vietnamese/tree/master
3)https://github.com/liuchengxu/blockchain-tutorial/blob/master/content/part-1/basic-prototype.md 

#РОАДМАП
1) https://roadmap.sh/blockchain

#YOUTUBE
1) https://www.youtube.com/playlist?list=PLpP5MQvVi4PGmNYGEsShrlvuE2B33xV1L
2) https://youtu.be/mTkIrOV8afs?si=IdqXognqa_ayNefF
3) https://youtu.be/qgofSZFTuVc?si=6g8hOc7smESe0i_G

#Ethereum
1) https://ethereum.org/ru/developers/docs/programming-languages/golang/

#Новости и статьи
1) https://www.mlq.ai/tag/blockchain/
