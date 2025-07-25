<template>
  <header class="site-header">
  <h1 class="site-title">Kids Connect</h1>
</header>
  <div class="page-container">
    
    <!-- Левая колонка -->
    <div class="main-content">
      <!-- Силовой спорт -->
      <h2 class="section-title">Силовой спорт</h2>
      <div v-for="(item, index) in sports.filter(s => strengthCategories.includes(s.category.toLowerCase()))" :key="'strength-' + index" class="card">
        <div class="card-left">
          <div class="image-placeholder" />
        </div>
        <div class="card-content">
          <div class="card-header">
            <div>
              <h3 class="title">
                {{ item.title }}
                <span class="location">{{ item.subtitle }}</span>
              </h3>
              <p class="category">#{{ item.category }}</p>
              <p class="info"><span class="icon">👥</span> {{ item.age }}</p>
              <p class="info"><span class="icon">📍</span> {{ item.address }}</p>
              <p class="info"><span class="icon">🏢</span> {{ item.place }}</p>
              <p class="info"><span class="icon">🕒</span> {{ item.days }}</p>
              <div class="times">
                <span v-for="(time, i) in item.times" :key="i" class="time">{{ time }}</span>
              </div>
            </div>
            <div class="card-actions">
              <div class="labels">
                <span v-if="item.free" class="free-label">Бесплатно</span>
                <span v-if="item.firstFree" class="first-free-label">Первое бесплатно</span>
                <span v-if="item.price" class="price-label">{{ item.price }}</span>
              </div>
              <button class="btn" @click="openModal(item)">Подробнее</button>

            </div>
          </div>
        </div>
      </div>

      <!-- Единоборства -->
      <h2 class="section-title">Единоборства</h2>
      <div v-for="(item, index) in sports.filter(s => combatCategories.includes(s.category.toLowerCase()))" :key="'combat-' + index" class="card">
        <div class="card-left">
          <div class="image-placeholder" />
        </div>
        <div class="card-content">
          <div class="card-header">
            <div>
              <h3 class="title">
                {{ item.title }}
                <span class="location">{{ item.subtitle }}</span>
              </h3>
              <p class="category">#{{ item.category }}</p>
              <p class="info"><span class="icon">👥</span> {{ item.age }}</p>
              <p class="info"><span class="icon">📍</span> {{ item.address }}</p>
              <p class="info"><span class="icon">🏢</span> {{ item.place }}</p>
              <p class="info"><span class="icon">🕒</span> {{ item.days }}</p>
              <div class="times">
                <span v-for="(time, i) in item.times" :key="i" class="time">{{ time }}</span>
              </div>
            </div>
            <div class="card-actions">
              <div class="labels">
                <span v-if="item.free" class="free-label">Бесплатно</span>
                <span v-if="item.firstFree" class="first-free-label">Первое бесплатно</span>
                <span v-if="item.price" class="price-label">{{ item.price }}</span>
              </div>
              <button class="btn" @click="openModal(item)">Подробнее</button>

            </div>
          </div>
        </div>
      </div>

      <!-- Гоночный спорт -->
      <h2 class="section-title">Гоночный спорт</h2>
      <div v-for="(item, index) in sports.filter(s => raceCategories.includes(s.category.toLowerCase()))" :key="'race-' + index" class="card">
        <div class="card-left">
          <div class="image-placeholder" />
        </div>
        <div class="card-content">
          <div class="card-header">
            <div>
              <h3 class="title">
                {{ item.title }}
                <span class="location">{{ item.subtitle }}</span>
              </h3>
              <p class="category">#{{ item.category }}</p>
              <p class="info"><span class="icon">👥</span> {{ item.age }}</p>
              <p class="info"><span class="icon">📍</span> {{ item.address }}</p>
              <p class="info"><span class="icon">🏢</span> {{ item.place }}</p>
              <p class="info"><span class="icon">🕒</span> {{ item.days }}</p>
              <div class="times">
                <span v-for="(time, i) in item.times" :key="i" class="time">{{ time }}</span>
              </div>
            </div>
            <div class="card-actions">
              <div class="labels">
                <span v-if="item.free" class="free-label">Бесплатно</span>
                <span v-if="item.firstFree" class="first-free-label">Первое бесплатно</span>
                <span v-if="item.price" class="price-label">{{ item.price }}</span>
              </div>
              <button class="btn" @click="openModal(item)">Подробнее</button>

            </div>
          </div>
        </div>
      </div>

      <!-- Скоростной спорт -->
      <h2 class="section-title">Скоростной спорт</h2>
      <div v-for="(item, index) in sports.filter(s => speedCategories.includes(s.category.toLowerCase()))" :key="'speed-' + index" class="card">
        <div class="card-left">
          <div class="image-placeholder" />
        </div>
        <div class="card-content">
          <div class="card-header">
            <div>
              <h3 class="title">
                {{ item.title }}
                <span class="location">{{ item.subtitle }}</span>
              </h3>
              <p class="category">#{{ item.category }}</p>
              <p class="info"><span class="icon">👥</span> {{ item.age }}</p>
              <p class="info"><span class="icon">📍</span> {{ item.address }}</p>
              <p class="info"><span class="icon">🏢</span> {{ item.place }}</p>
              <p class="info"><span class="icon">🕒</span> {{ item.days }}</p>
              <div class="times">
                <span v-for="(time, i) in item.times" :key="i" class="time">{{ time }}</span>
              </div>
            </div>
            <div class="card-actions">
              <div class="labels">
                <span v-if="item.free" class="free-label">Бесплатно</span>
                <span v-if="item.firstFree" class="first-free-label">Первое бесплатно</span>
                <span v-if="item.price" class="price-label">{{ item.price }}</span>
              </div>
              <button class="btn" @click="openModal(item)">Подробнее</button>

            </div>
          </div>
        </div>
      </div>
    </div>


  <!-- Правая колонка -->
  <aside class="sidebar">
    <div class="search-panel">
      <input type="text" class="search" placeholder="Поиск" />
      <div class="filter-buttons">
        <button class="filter-btn">Все</button>
        <button class="filter-btn">Платные</button>
        <button class="filter-btn">Бесплатные</button>
      </div>
    </div>

    <div class="filters">
      <h3>Фильтры</h3>
      <label>
        Возраст
        <select>
          <option>Любой</option>
          <option>10-12</option>
          <option>13-15</option>
          <option>16-18</option>
        </select>
      </label>

      <div class="gender">
        <label><input type="checkbox" checked /> Мужской</label>
        <label><input type="checkbox" checked /> Женский</label>
      </div>

      <div class="catalog">
        <p>Каталог</p>
        <ul>
          <li>
            ▸ Силовой спорт <span class="count">3</span>
            <ul>
              <li>- Тяжелая атлетика <span class="count">3</span></li>
              <li>- Пауэрлифтинг <span class="count">1</span></li>
            </ul>
          </li>
          <li>
            ▸ Единоборства <span class="count">2</span>
            <ul>
              <li>- Вольная борьба <span class="count">1</span></li>
              <li>- Дзюдо <span class="count">1</span></li>
            </ul>
          </li>
          <li>
            ▸ Гоночный спорт
            <ul>
              <li>- Картинг</li>
              <li>- Мотокросс</li>
            </ul>
          </li>
          <li>
            ▸ Скоростной спорт
            <ul>
              <li>- Бег 100м</li>
              <li>- Велоспорт</li>
            </ul>
          </li>
          <li>▸ ДПИ и ремесла</li>
          <li>▸ Техническое конструирование</li>
          <li>▸ Словесность</li>
          <li>▸ Иностранные языки</li>
          <li>▸ Развитие интеллекта</li>
        </ul>
      </div>
    </div>
  </aside>
</div>

  <!-- 🟥 МОДАЛКА ПОД СКРИН -->
<div v-if="showModal && selectedItem" class="modal-overlay" @click.self="closeModal">
  <div class="modal-content">
    <header class="modal-header">
      <h1 class="site-title">Kids Connect</h1>
    </header>

    <div class="modal-body">
      <button class="back-btn" @click="closeModal">← Назад</button>

      <h2>{{ selectedItem.title }} ({{ selectedItem.subtitle }})</h2>

<!-- Картинка (пустая заглушка, как на сайте) -->
<div class="section-placeholder">
  <span>Нет изображения</span>
</div>


      <!-- Метки -->
      <div class="labels">
        <span class="badge" v-if="selectedItem.status">Набор открыт</span>
        <span class="badge free" v-if="selectedItem.free">Бесплатно</span>
      </div>

      <!-- Инфо -->
      <div class="info-block">
        <p><strong>👥 Возраст:</strong> {{ selectedItem.age }}</p>
        <p><strong>📍 Адрес:</strong> {{ selectedItem.address }}</p>
        <p><strong>🏢 Место:</strong> {{ selectedItem.place }}</p>
      </div>
      

      <!-- Описание -->
<div class="description-block">
  <h3>ОПИСАНИЕ</h3>
  <p>{{ selectedItem.description || 'Описание секции временно отсутствует.' }}</p>
</div>

<!-- Содержание программы -->
<div class="content-block">
  <h3>СОДЕРЖАНИЕ ПРОГРАММЫ</h3>
  <p>{{ selectedItem.content || 'Информация о содержании программы будет добавлена позже.' }}</p>
</div>


      <!-- Группы -->
      <div class="group-block">
        <h3>ГРУППЫ</h3>
        <div class="group-info">
          <p><strong>Этап:</strong> Этап начальной подготовки</p>
          <p><strong>Тренер:</strong> Петрова Елена Александровна</p>
          <p><strong>Время:</strong> 15 и 20</p>
          <p><strong>Срок обучения:</strong> 12 месяцев</p>
        </div>
      </div>

      <!-- Расписание -->
      <div class="schedule-block">
        <h3>РАСПИСАНИЕ ЗАНЯТИЙ</h3>
        <div class="days">
          <p>📅 Пн, Вт, Чт, Сб</p>
          <div class="times">
            <span class="time-tag">08:00 - 10:00</span>
            <span class="time-tag">18:00 - 19:30</span>
          </div>
        </div>
      </div>

      <!-- Действия -->
      <div class="action-block">
        <button class="btn primary">Записаться</button>
        <button class="btn ghost">На карте 📍</button>
      </div>
    </div>
  </div>
</div>


</template>

<script setup>
const strengthCategories = ['тяжелая атлетика', 'пауэрлифтинг', 'армреслинг']
const combatCategories = ['дзюдо', 'вольная борьба', 'каратэ', 'бокс']
const raceCategories = ['картинг', 'мотокросс']
const speedCategories = ['бег', 'велоспорт']

const sports = [
  { title: 'Тяжелая атлетика', subtitle: '(в Юбилейном мкр.)', category: 'тяжелая атлетика', age: '10-18 лет', address: 'г. Иркутск, Юбилейный мкр., стр. 49/1', place: 'ФОК "Юбилейный"', days: 'Пн, Ср, Пт', times: ['09:00 - 10:30', '12:00 - 13:30', '18:00 - 19:30'], free: true },
  { title: 'Тяжелая атлетика', subtitle: '(на ул. Боткина)', category: 'тяжелая атлетика', age: '10-18 лет', address: 'г. Иркутск, ул. Боткина, 15', place: 'СК "Атлет"', days: 'Пн, Ср, Пт', times: ['09:00 - 10:30', '12:00 - 13:30'], firstFree: true, price: '500 руб.' },
  { title: 'армреслинг', subtitle: '(в Юбилейном мкр.)', category: 'армреслинг', age: '10-18 лет', address: 'г. Иркутск, Юбилейный мкр., стр. 49/1', place: 'ФОК "Юбилейный"', days: 'Пн, Ср, Пт', times: ['09:00 - 10:30', '12:00 - 13:30', '18:00 - 19:30'], free: true },
  { title: 'Дзюдо', subtitle: '', category: 'дзюдо', age: '6–18 лет', address: 'г. Иркутск, ул Трудовая, д 115А', place: 'СК "Рингспец"', days: 'Пн, Ср, Пт', times: ['09:00 - 10:30', '12:00 - 13:30'], free: true },
  { title: 'Каратэ', subtitle: '', category: 'каратэ', age: '8–16 лет', address: 'г. Иркутск, ул Спортивная, 22', place: 'ДЮСШ "Спарта"', days: 'Вт, Чт', times: ['17:00 - 18:30'], price: '1000 руб.', firstFree: true },
  { title: 'Бокс', subtitle: '', category: 'бокс', age: '12–18 лет', address: 'г. Иркутск, ул Ленина, 9', place: 'СК "Чемпион"', days: 'Пн, Ср, Пт', times: ['16:00 - 17:30'], free: true },
  { title: 'Картинг', subtitle: '', category: 'картинг', age: '10–17 лет', address: 'г. Иркутск, ул Дорожная, 30', place: 'Автодром Юниор', days: 'Сб, Вс', times: ['11:00 - 13:00'], price: '1500 руб.' },
  { title: 'Мотокросс', subtitle: '', category: 'мотокросс', age: '12–18 лет', address: 'г. Иркутск, ул Окружная, 9', place: 'Трасса "Вихрь"', days: 'Сб', times: ['14:00 - 16:00'], firstFree: true },
  { title: 'Бег 100м', subtitle: '', category: 'бег', age: '10–16 лет', address: 'г. Иркутск, ул Ленина, 2', place: 'Стадион "Центральный"', days: 'Вт, Чт', times: ['17:00 - 18:30'], free: true },
  { title: 'Велоспорт', subtitle: '', category: 'велоспорт', age: '10–17 лет', address: 'г. Иркутск, ул Байкальская, 45', place: 'Спортпарк "Байкал"', days: 'Ср, Пт', times: ['10:00 - 11:30'], price: '800 руб.' }
]


import { ref } from 'vue'

const selectedItem = ref(null)
const showModal = ref(false)

function openModal(item) {
  selectedItem.value = item
  showModal.value = true
}

function closeModal() {
  showModal.value = false
}


</script>



<style scoped>
.site-header {
  background: linear-gradient(90deg, #7d0c25 0%, #a3162f 100%);
  color: white;
  padding: 20px 40px;
  border-radius: 16px;
  text-align: center;
  margin-bottom: 30px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.site-title {
  font-size: 36px;
  font-weight: 800;
  letter-spacing: 1px;
  margin: 0;
  font-family: 'Segoe UI', sans-serif;
}

.page-container {
  display: flex;
  background-color: #f5f5f5;
  padding: 20px;
  gap: 20px;
}

.main-content {
  flex: 1;
}

.sidebar {
  width: 300px;
  background-color: #fff;
  padding: 16px;
  border-radius: 8px;
  box-shadow: 0 0 4px rgba(0, 0, 0, 0.1);
}

.section-title {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 20px;
}

.card {
  background: #fff;
  padding: 16px;
  border-radius: 12px;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
  margin-bottom: 16px;
  display: flex;
  gap: 12px;
}

.card-left {
  width: 100px;
  height: 100px;
}

.image-placeholder {
  width: 100px;
  height: 100px;
  background-color: #ddd;
  border-radius: 8px;
}

.card-content {
  flex: 1;
}

.card-header {
  display: flex;
  justify-content: space-between;
}

.title {
  font-size: 18px;
  font-weight: 600;
  margin: 0;
}

.location {
  font-weight: normal;
  color: #666;
  font-size: 15px;
  margin-left: 4px;
}

.category {
  color: #c33;
  font-size: 14px;
  margin: 4px 0;
}

.info {
  font-size: 14px;
  color: #444;
  margin: 2px 0;
}

.icon {
  margin-right: 5px;
}

.times {
  margin-top: 6px;
}

.time {
  background: #fcd48c;
  padding: 4px 10px;
  border-radius: 6px;
  margin-right: 6px;
  font-size: 13px;
  font-weight: 500;
}

.card-actions {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: space-between;
}

.labels {
  display: flex;
  flex-direction: column;
  gap: 4px;
  align-items: flex-end;
}

.free-label {
  background-color: #ffd9dd;
  padding: 4px 8px;
  border-radius: 6px;
  font-size: 13px;
  font-weight: 500;
}

.first-free-label {
  background-color: #e6f1ff;
  padding: 4px 8px;
  border-radius: 6px;
  font-size: 13px;
}

.price-label {
  background-color: #fce2b6;
  padding: 4px 8px;
  border-radius: 6px;
  font-size: 13px;
  font-weight: 500;
}

.btn {
  margin-top: 10px;
  background-color: #7d0c25;
  color: white;
  border: none;
  border-radius: 8px;
  padding: 8px 16px;
  cursor: pointer;
  font-weight: bold;
}

.search-panel {
  margin-bottom: 20px;
}

.search {
  width: 100%;
  padding: 8px;
  margin-bottom: 10px;
  border: 1px solid #ccc;
  border-radius: 8px;
}

.filter-buttons {
  display: flex;
  gap: 10px;
}

.filter-btn {
  flex: 1;
  padding: 6px 12px;
  border: 1px solid #ccc;
  border-radius: 6px;
  background: white;
  cursor: pointer;
  font-size: 14px;
}

.filters h3 {
  margin-bottom: 12px;
  font-size: 18px;
}

.filters label, .filters select {
  display: block;
  margin-bottom: 10px;
  font-size: 14px;
  width: 100%;
}

.gender label {
  display: block;
  margin-bottom: 6px;
}

.catalog ul {
  list-style: none;
  padding-left: 0;
}

.catalog li {
  margin-bottom: 6px;
}

.count {
  color: #999;
  font-size: 13px;
  margin-left: 6px;
}

.modal-overlay {
  position: fixed;
  inset: 0;
  background-color: rgba(0,0,0,0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
  overflow-y: auto;
  padding: 20px;
}

.modal-content {
  background: white;
  border-radius: 12px;
  /* Увеличено примерно в 2 раза */
  max-width: 1400px;
  width: 100%;
  max-height: 90vh;
  overflow-y: auto;
  box-shadow: 0 4px 30px rgba(0,0,0,0.3);
  padding: 40px 60px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 18px; /* чуть крупнее */
}

.modal-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.back-btn {
  background: none;
  border: none;
  font-size: 20px;
  cursor: pointer;
  color: #7d0c25;
  font-weight: 600;
  margin-bottom: 30px;
}

.section-placeholder {
  width: 100%;
  height: 360px; /* увеличена */
  background-color: #ddd;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #666;
  font-size: 36px; /* увеличен */
  margin-bottom: 15px;
  user-select: none;
}

.labels {
  display: flex;
  gap: 20px;
  margin-bottom: 25px;
}

.badge {
  background-color: #7d0c25;
  color: white;
  padding: 10px 20px;
  border-radius: 12px;
  font-weight: 600;
  font-size: 18px;
  user-select: none;
}

.badge.free {
  background-color: #ffd9dd;
  color: #7d0c25;
}

.info-block p {
  margin: 10px 0;
  font-size: 18px;
  color: #333;
}

.description-block, .content-block, .group-block, .schedule-block {
  margin-top: 40px;
}

.description-block h3,
.content-block h3,
.group-block h3,
.schedule-block h3 {
  margin-bottom: 16px;
  color: #7d0c25;
  font-weight: 700;
  font-size: 28px;
}

.group-info p, .days p {
  margin: 8px 0;
  font-size: 16px;
  color: #444;
}

.times {
  margin-top: 12px;
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}

.time-tag {
  background: #fcd48c;
  padding: 10px 24px;
  border-radius: 12px;
  font-weight: 600;
  font-size: 18px;
}

.action-block {
  margin-top: 50px;
  display: flex;
  gap: 24px;
  justify-content: flex-start;
}

.btn.primary {
  background-color: #7d0c25;
  color: white;
  border: none;
  padding: 20px 50px;
  border-radius: 12px;
  font-weight: 700;
  cursor: pointer;
  font-size: 22px;
}

.btn.ghost {
  background: none;
  border: 2px solid #7d0c25;
  color: #7d0c25;
  padding: 20px 50px;
  border-radius: 12px;
  font-weight: 700;
  cursor: pointer;
  font-size: 22px;
}

@media (max-width: 768px) {
  .modal-content {
    max-width: 100%;
    padding: 30px 40px;
    font-size: 16px;
  }
  .section-placeholder {
    height: 220px;
    font-size: 24px;
  }
  .description-block h3,
  .content-block h3,
  .group-block h3,
  .schedule-block h3 {
    font-size: 22px;
  }
  .time-tag {
    padding: 8px 18px;
    font-size: 16px;
  }
  .btn.primary, .btn.ghost {
    padding: 16px 36px;
    font-size: 18px;
  }
}

/* Плавное появление модалки */
.modal-overlay {
  animation: fadeIn 0.3s ease forwards;
  background-color: rgba(0, 0, 0, 0.5);
  position: fixed;
  inset: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

/* Градиент для кнопок */
.btn {
  background: linear-gradient(135deg, #7d0c25, #a3162f);
  transition: background 0.3s ease;
  display: inline-flex;
  align-items: center;
  gap: 6px;
}
.btn:hover {
  background: linear-gradient(135deg, #a3162f, #7d0c25);
}

/* Иконка стрелка для кнопки Подробнее */
.btn .icon-arrow {
  display: inline-block;
  border: solid white;
  border-width: 0 2px 2px 0;
  padding: 3px;
  transform: rotate(45deg);
  margin-left: 6px;
}

/* Кнопка "Подробнее" с иконкой */
.card-actions .btn {
  font-weight: 700;
}

/* Иконка для кнопки "Записаться" */
.action-block .btn.primary::before {
  content: "📝";
  margin-right: 8px;
}

/* Hover эффект для карточек */
.card:hover {
  box-shadow: 0 8px 20px rgba(125, 12, 37, 0.3);
  transform: translateY(-3px);
  transition: all 0.3s ease;
}

/* Подсветка выбранной категории в боковой панели */
.filter-btn.active {
  background-color: #a3162f;
  color: white;
  font-weight: 700;
  border-radius: 8px;
}

/* Курсор pointer для интерактивных элементов */
.filter-btn, .btn {
  cursor: pointer;
}

/* Кнопка назад в модалке — курсор и эффект */
.back-btn {
  cursor: pointer;
  color: #7d0c25;
  font-weight: 600;
  border: none;
  background: none;
  font-size: 16px;
  margin-bottom: 15px;
  transition: color 0.2s ease;
}
.back-btn:hover {
  color: #a3162f;
}


.filter-buttons {
  display: flex;
  gap: 14px;
  flex-wrap: wrap;
}

.filter-btn {
  flex: 1;
  padding: 10px 14px;
  border-radius: 14px;
  border: 2px solid #7d0c25;
  background: white;
  color: #7d0c25;
  font-weight: 600;
  font-size: 15px;
  text-align: center;
  cursor: pointer;
  user-select: none;
  transition: all 0.3s ease;
  box-shadow: 0 3px 6px rgba(125, 12, 37, 0.1);
}

.filter-btn:hover {
  background: #7d0c25;
  color: white;
  box-shadow: 0 6px 15px rgba(125, 12, 37, 0.3);
  border-color: #a3162f;
}

.filter-btn.active {
  background: linear-gradient(135deg, #7d0c25, #a3162f);
  color: white;
  border: none;
  box-shadow: 0 8px 25px rgba(163, 22, 47, 0.6);
}

/* Для удобства на мобильных */
@media (max-width: 480px) {
  .filter-buttons {
    flex-direction: column;
  }
  .filter-btn {
    flex: unset;
    width: 100%;
  }
}
/* Правая колонка */
.sidebar {
  width: 280px;
  padding: 20px;
  background: #fff;
  border-left: 1px solid #ddd;
  font-family: Arial, sans-serif;
  font-size: 14px;
  color: #333;
  max-height: 700px;
}

.search-panel {
  margin-bottom: 20px;
}

.search {
  width: 100%;
  padding: 8px 12px;
  border: 1px solid #ccc;
  border-radius: 6px;
  font-size: 14px;
  box-sizing: border-box;
  outline-offset: 2px;
  transition: border-color 0.3s ease;
}

.search:focus {
  border-color: #d6336c;
}

.filter-buttons {
  margin-top: 10px;
  display: flex;
  gap: 8px;
}

.filter-btn {
  flex: 1;
  padding: 6px 0;
  border: 1px solid #ccc;
  background: #f9f9f9;
  border-radius: 6px;
  cursor: pointer;
  font-weight: 600;
  transition: background-color 0.3s ease, border-color 0.3s ease;
  user-select: none;
}

.filter-btn:hover {
  background-color: #f3e1e5;
}

.filter-btn.active {
  background-color: #d6336c;
  color: white;
  border-color: #d6336c;
}

.filters h3 {
  margin-top: 0;
  margin-bottom: 10px;
  font-weight: 700;
  font-size: 16px;
  color: #d6336c;
}

.filters label {
  display: block;
  margin-bottom: 12px;
  font-weight: 600;
}

.filters select {
  margin-top: 4px;
  width: 100%;
  padding: 6px 8px;
  border-radius: 6px;
  border: 1px solid #ccc;
  font-size: 14px;
  box-sizing: border-box;
}

.gender {
  margin-bottom: 20px;
}

.gender label {
  display: inline-flex;
  align-items: center;
  margin-right: 12px;
  font-weight: 500;
  cursor: pointer;
}

.gender input[type="checkbox"] {
  margin-right: 6px;
}

/* Каталог */
.catalog p {
  font-weight: 700;
  font-size: 16px;
  margin-bottom: 10px;
  color: #d6336c;
}

.catalog-list {
  list-style: none;
  padding-left: 0;
  margin: 0;
}

.catalog-list > li {
  margin-bottom: 8px;
  position: relative;
  padding-left: 24px;
  cursor: default;
  user-select: none;
}

/* Кнопка-треугольник */
.catalog-toggle {
  position: absolute;
  left: 0;
  top: 2px;
  border: none;
  background: none;
  font-size: 14px;
  cursor: pointer;
  padding: 0;
  line-height: 1;
  user-select: none;
  transition: transform 0.3s ease;
}

/* Поворот треугольника при раскрытии */
.catalog-toggle.open {
  transform: rotate(90deg);
}

/* Подкаталог по умолчанию скрыт */
.subcatalog {
  margin-top: 6px;
  margin-left: 20px;
  list-style: none;
  padding-left: 0;
  display: none;
  color: #555;
  font-weight: 400;
  font-size: 13px;
}

.subcatalog li {
  margin-bottom: 4px;
}

/* Показываем подкаталог при открытии */
.subcatalog.open {
  display: block;
}

/* Счётчики рядом с пунктами */
.count {
  background-color: #d6336c;
  color: white;
  font-size: 11px;
  padding: 1px 5px;
  border-radius: 12px;
  margin-left: 6px;
  font-weight: 700;
}
.catalog-toggle::before {
  content: "▶";
  display: inline-block;
  transition: transform 0.3s ease;
}

.catalog-toggle.open::before {
  transform: rotate(90deg);
}


</style>
