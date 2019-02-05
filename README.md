
## Дикларация (DOCTYPE)
**С чего начинается HTML-документ?**

Любой HTML-документ начинается с дикларации (типа документа еще его называют доктайп).
Тип документа нужен, чтобы браузер мог определить версию HTML и правильно отобразить страницу. Доктайп помещают в самый вверх страницы (далее вы увидите в примерах).
```html
<!DOCTYPE html>
```
**Что будет если не указывать дикларацию?**

Если не указывать дикларацию то браузер перейдет в **режим совместимости**. Этот режим предназначен для отображения веб-страницы подобно старым браузерам. В режиме совместимости игнорируются стандарты HTML и CSS, и поведение браузеров становится непредсказуемым. Для переключения в режим совместимости существует множество доктайпов, вот лишь некоторые из них.
```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Frameset//EN">

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN">
```
_Подробнее про **режим совместимости** вы можите найти в интернете._ 






## Счетчик просмотров

```php
    /**
     * @return bool
     * @throws \Exception
     * @throws \Throwable
     * @throws \yii\db\StaleObjectException
     */
    public function processCountViewPost()
    {
        $session = Yii::$app->session;
        // Если в сессии отсутствуют данные,
        // создаём, увеличиваем счетчик, и записываем в бд
        if (!isset($session['blog_post_view'])) {
            $session->set('blog_post_view', [$this->id]);
            $this->update(['view' => 1]);
            // Если в сессии уже есть данные то проверяем засчитывался ли данный пост
            // если нет то увеличиваем счетчик, записываем в бд и сохраняем в сессию просмотр этого поста
        } else {
            if (!ArrayHelper::isIn($this->id, $session['blog_post_view'])) {
                $array = $session['blog_post_view'];
                array_push($array, $this->id);
                $session->remove('blog_post_view');
                $session->set('blog_post_view', $array);
                $this->updateCounters(['view' => 1]);
            }
        }
        return true;
    } 
    
    
     /**
     * @param $id
     * @return string
     * @throws NotFoundHttpException
     * @throws \Exception
     * @throws \Throwable
     * @throws \yii\db\StaleObjectException
     */
    public function actionView($id)
    {
        $model = $this->findModel($id);
        $model->processCountViewPost();

        return $this->render('view', [
            'model' => $model,
        ]);
    }
```
