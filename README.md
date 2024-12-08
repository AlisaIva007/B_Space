# B_Space
# Определение персонажей игры.
define A = Character('Алекс', color="#c8ffc8")
#кеп
define AM = Character('Алекс(мысли)', color="#c8ffc8")
#мысли гг
define B = Character('Вольт',color="#c3ffc9")
#программмист
define a = Character('Анна', color="#c8ffc8")
#мед
define I = Character('Ива', color="#c8ffc8")
#биоинж
define G = Character('Голли', color="#c8ffc8")
#пасечник
#все по старту творцы
# Вместо использования оператора image можете просто
# складывать все ваши файлы изображений в папку images.
# Например, сцену bg room можно вызвать файлом "bg room.png",
# а eileen happy — "eileen happy.webp", и тогда они появятся в игре.

# Игра начинается здесь:
label start:
    scene spacee
    with dissolve

    show eileen happy

    AM "Эх...давно это было. Когда первое, что ты видел утром не бескрайний космос, а ослепительное солнце.."
    AM "Приятные лучики солнца падали на лицо, из-за чего так и хотелось улыбаться!"
    AM "Уже больше месяца мы путешествуем на нашем корабле по космосу. " 
    scene bort 
    show eileen happy at right

    B "Кеп, по моим расчетам через день-два мы будем пролетать мимо планеты Умарталык."
    AM "что-то я погрузился в мысли.. "
    show eileen happy at left
    A "Вольт, держим курс на Умарталык, будем приземляться и исследовать землю."
    show eileen happy at right
    B "Так точно, капитан!"
    show eileen happy at left
    A "Вольт,просмотри пока обитателей планеты и приготовь отчет"
    show eileen happy at right
    B "Точно..Алекс, тебя искала Ива"
    show eileen happy at left
    A "Понял,тогда я зайду к ней, а ты остаешься за главного"
    show eileen happy at right
    B "Как скажешь"



    scene zone
    AM "Интересно, зачем Ива искала меня?"

    scene 12
    show eileen happy
    I "O! А вот и ты, Алекс!!"
    show eileen happy
    I "Доброе утречко!"
    show eileen happy at left
    A "Доброе, Ива"
    show eileen happy at left
    A "Мне сказали, что ты искала меня, что-то случилось?"
    show eileen happy at right
    I "Да, искала"
    show eileen happy at right
    I "Нам хватит меда максимум на дней пять!!!"
    show eileen happy at right
    I "Нам срочно нужно пополнить запасы топлива и провианта!"
    show eileen happy at left
    A "Не переживай, мы с Вольтом держим курс на ближайшую к нам планету"
    show eileen happy at right
    I "Ох..правда? А что за планета?"
    show eileen happy at left
    A "Умарталык"
    show eileen happy at right
    I "Хм..надо глянуть в архивах про нее"
    show eileen happy at left
    A "Вольт как раз этим и занимается"
    show eileen happy at left
    A "Если так сильно переживаешь, можем зайти к Вольту и узнать все у него"
    show eileen happy at right
    I "Давай! Только я также хотела показать доклад о состоянии Берлоги"
    show eileen happy at left
    A "Не думал, что ты его так быстро сделаешь.."
    menu:
        "Что делать?"

        "Похвалить Иву":
            jump rep

        "Отругать":
            jump ne_rep
    return
label rep:
    show eileen happy at left
    A "Молодец. Видно, что ты стараешься"
    show eileen happy at right
    I "Спасибо, Алекс!"
    return

label ne_rep:
    show eileen happy at left
    A "Спешить - медведей насмешить..Ты точно все проверила?"
    show eileen happy at right
    I "Ох..теперь я сама не уверенна, что все сделала правильно"
    return
