---
title: 'fju_dataset_formats'
# titie: 'Seminar - '
date: "2022-05-25"
theme: theme/mytheme.css
output: html_document
---

# FJU chatbot Dataset Format <!-- .element: class="title" -->

<div class="title-name">
2022.05.25 <br>
Yu-Hung Wu @ IIS, Academia Sinica
</div>

---

## Dataset

* The dataset are converted in JSON format.

```json
{
  "category":"relationship",
  "dialogue":[
    {
      "utterance":"我覺得跟阿公阿嬤好像很難聊天",
      "speaker":"user"
    },
    {
      "utterance":"怎麼會，你們不常見面嗎",
      "speaker":"bot"
    },
    {
      "utterance":"也不是，一個禮拜一次啊",
      "speaker":"user"
    },
    {
      "utterance":"那你有沒有學著好好聽他們說話",
      "speaker":"bot"
    },
    {
      "utterance":"沒有耶…",
      "speaker":"user"
    },
    {
      "utterance":"他們可能很想跟你分享，你下次可以試著問問他們之前小時候的故事啊～",
      "speaker":"bot"
    },
    {
      "utterance":"我下次努力試試～他們其實平時也很關心我",
      "speaker":"user"
    },
    {
      "utterance":"對啊，或你也可以關心他們一下，像有沒有睡好啊，吃飽沒之類的",
      "speaker":"bot"
    },
    {
      "utterance":"我知道了，我會努力的",
      "speaker":"user"
    },
    {
      "utterance":"加油加油！",
      "speaker":"bot"
    }
  ],
  "id":"4e90b44c-87b9-4764-a675-5f1c95233f0d",
  "university":"fju",
  "date":"20211201"
}
```

---

## Dataset.

* Each element represents a dialogue.

* Specification of each element:
  * ```category```: ```str```, represents the category of the dialogue.
    * Must be one of these: [food(食), clothing(衣), housing(住), transportation(行), education(育), entertainment(樂/生活), relationship(人際關係), club(社團), work(工作/打工), covid(疫情)]
  * ```dialogue```: ```list```, Contains the utterances.
  * ```id```: ```str```, an unique id.
  * ```university```: ```str```, source of the dialogue.
    * Must be one of these: [fju(輔仁), ntue(國北教)]
  * ```date```: ```str```.

---

## Statistics

| Category       | 下新莊區輔仁大學 | 差點被台大合併的國北教 | **Total**  |
| -------------- | ---------------- | ---------------------- | ---------- |
| food           | 172              | 92                     | 264        |
| clothing       | 234              | 0                      | 234        |
| housing        | 102              | 23                     | 125        |
| transportation | 168              | 61                     | 229        |
| education      | 275              | 127                    | 402        |
| entertainment  | 383              | 232                    | 615        |
| club           | 33               | 0                      | 33         |
| relationship   | 145              | 149                    | 294        |
| work           | 20               | 21                     | 41         |
| covid          | 40               | 0                      | 40         |
| **total**      | 1572             | 705                    | ***2277*** |