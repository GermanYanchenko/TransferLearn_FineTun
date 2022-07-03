# Transfer Learning и Fine Tuning
Как и в https://github.com/GermanYanchenko/ImageClass_binary выполнен классификатор кошек и собак.<br>
Применив transfer learning в качестве базовой модели была выбрана cеть MobileNet.Заморозив сеть и добавив полносвязный слой на выходе было произведено обучение.
Метрика качества - точность, оптимизатор - адам, функция потерь - кросс-энтропия. История обучения представлена ниже: <br>

![alt text](https://github.com/GermanYanchenko/TransferLearn_FineTun/blob/main/image/hist_trans_learn.png?raw=true)<br>
Точность на валидации составила 95,9%. <br>
Далее с помощью fine tuning были разморожены последние 54 слоя из 154, а затем выполнено дообучение. История обучения: <br>

![alt text](https://github.com/GermanYanchenko/TransferLearn_FineTun/blob/main/image/hist_fine_tun.png?raw=true)<br>
Точность на валидации увеличилась и составила 96,8%, но видны небольшие признаки переобучения.(точность на тренировочном датасете 99,7%). <br>
Предсказание итоговой модели:<br>

![alt text](https://github.com/GermanYanchenko/TransferLearn_FineTun/blob/main/image/predict_tl_ft.png?raw=true)<br>
