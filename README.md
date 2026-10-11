# Brightmoss: a bright family dental practice site with a Formgong form

**Live demo:** https://brightmoss.formgong.com · Download: the [latest release](https://github.com/formgong/brightmoss-template/releases/latest) zip.

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/formgong/brightmoss-template) [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fformgong%2Fbrightmoss-template&project-name=brightmoss&repository-name=brightmoss)

Each button copies the site to your GitHub and publishes it. Then replace `fk_your_access_key` in `index.html` of your copy with your Formgong access key (free at https://formgong.com/new) and commit: the host republishes on its own.

Яскравий сайт сімейної стоматології з формою Формгонг

A cheerful one-page site for a family or children's dental practice, in a single `index.html` plus an `img/` folder. The demo practice, Brightmoss Dental in the town of Tansy Cross, its team, reviews, prices, addresses and phone number are fictional sample content.

- **Intro.** A short opening: a sun rises behind the tooth mark, the name slides up, then the cream curtain lifts off the page.
- **Header.** Transparent over the green hero, it turns into a cream pill once you scroll. A yellow pill slides behind the menu item of the section you are reading. On phones it becomes a menu button with a full-screen menu.
- **Hero.** A rounded green panel with a big headline, a tall photo that wipes in from the bottom, a framed photo with a spinning "kids welcome" badge, a sun behind it, a booking button and the emergency phone number.
- **Why families choose us.** A large statement whose words light up one by one as you scroll, with three photos drifting past at different speeds.
- **Treatments.** Six colourful cards (check-ups, children, hygiene, emergency, clear aligners, whitening) plus an "ask us" card. Each one lifts on hover, and a click picks that treatment in the form.
- **Emergency care.** A coral band with a call button that gently pulses.
- **Plans and prices.** Pay-as-you-go next to a monthly Family Plan, then a price list with tabs.
- **How a first visit works.** On wide screens a wheel turns as you scroll and brings each of the five steps to the top. On phones it is a simple list.
- **Team.** Four portraits in a staggered row that move at a slightly different speed.
- **Practices.** Two locations with addresses and opening hours, and three numbers that count up.
- **Reviews.** Sample reviews running in a slow loop that stops when you hover.
- **FAQ.** Two groups of questions that open and close.
- **Booking.** A green section with the phone, email and hours next to the appointment request form.
- **Footer.** Addresses, treatments, contact details and a giant wordmark whose letters rise in turn.

Blocks rise into view as you scroll. Without JavaScript everything is visible and the price list shows all its tabs. With `prefers-reduced-motion: reduce` there is no intro and nothing moves.

## English

**Set up the form**

1. Create a form in the Formgong dashboard and copy its access key.
2. In `index.html`, replace `fk_your_access_key` with that key.
3. The form sends `name`, `email`, `phone`, `service`, `patient`, `practice`, `preferred_time`, `message`, the hidden `subject` and the empty honeypot `botcheck`. Name and email are required; everything else is optional or has a default. It shows thanks only when Formgong answers `success: true`. Otherwise it shows the error and keeps what was typed.

**Edit**

- Colours are at the top of the styles: `--leaf` for the hero, the booking section and buttons, `--sun` for buttons and highlights, `--coral` for emergency care, `--ink` for text, the visit wheel and the footer, `--cream` for the page and `--sprout` for the light green panels.
- Fonts: Bricolage Grotesque for headings and Figtree for text, both from Google Fonts.
- Treatments are `<a class="svc">` cards. `data-service` must match a `value` in the form's treatment chips so a click can pick it.
- The visit steps are the `<li class="step">` items. If you add or remove a step, add or remove a `wheel-dot` too.
- Prices live in the `.panel` lists under "Price list". The numbers in "Practices" count up to their `data-count` value.
- Replace the photos in `img/`, keeping the file names, or change the paths in `index.html`. Until a photo exists, its frame shows a soft colour instead.

**Images.** The eleven photos were generated for this template with ChatGPT image generation (OpenAI) and saved as WebP, about 1.2 MB in all. The prompts are in `img-prompts.json`. The people and places are fictional. You may use them in your own site, but replace them with photos of your own practice and team before launch.

**Health data.** This form is for appointment requests. Don't use it to collect diagnoses, medical history, prescriptions or insurance numbers; keep those in your clinic's own patient system. The note field carries a reminder not to include medical details.

**Sample content.** The reviews, the team, the prices, the plan, the addresses and the phone number are made up for the demo. Replace them with your own before you publish.

## Українська

Яскравий односторінковий сайт для сімейної або дитячої стоматології: один файл `index.html` і тека `img/`. Клініка Brightmoss Dental у містечку Tansy Cross, її команда, відгуки, ціни, адреси й телефон вигадані для прикладу.

На сторінці:

- коротке вступне відкриття: за логотипом сходить сонце, потім завіса підіймається;
- шапка, прозора над зеленим першим екраном, яка під час прокрутки стає кремовою «пігулкою»; жовта «пігулка» під пунктом меню показує розділ, який ви читаєте; на телефоні це кнопка меню;
- перший екран із великим заголовком, фото, що відкривається знизу, фото в рамці з бейджем, що обертається, кнопкою запису й телефоном для термінових випадків;
- великий вислів, слова якого засвічуються під час прокрутки, і три фото, що пропливають з різною швидкістю;
- шість кольорових карток послуг і картка «не знаєте, що потрібно?»: клік вибирає послугу у формі;
- коралова смуга про невідкладну допомогу з кнопкою дзвінка;
- оплата за візит поруч із сімейним планом і прайс із вкладками;
- «як проходить перший візит»: на широкому екрані колесо повертається під час прокрутки, на телефоні це простий список;
- команда з чотирьох людей;
- дві клініки з адресами й годинами роботи та цифри, що рахуються;
- відгуки, що повільно біжать по колу;
- запитання й відповіді;
- зелений блок запису з формою;
- футер із великим логотипом.

**Налаштування форми.** Створіть форму в кабінеті Formgong і замініть `fk_your_access_key` у `index.html` на свій ключ. Форма надсилає `name`, `email`, `phone`, `service`, `patient`, `practice`, `preferred_time`, `message`, приховані `subject` і `botcheck`. Обов'язкові ім'я та email. Подяка з'являється лише тоді, коли Formgong відповідає `success: true`; інакше форма показує помилку й зберігає введене.

**Редагування.** Кольори задані на початку стилів (`--leaf`, `--sun`, `--coral`, `--ink`, `--cream`, `--sprout`). Шрифти: Bricolage Grotesque для заголовків і Figtree для тексту. У картки послуг `data-service` має збігатися зі значенням у кнопках вибору послуги у формі. Ціни змінюйте у списках `.panel`, цифри в блоці клінік — в атрибуті `data-count`. Фото замініть у теці `img/`, зберігши назви файлів; поки фото немає, на його місці м'який кольоровий фон.

**Зображення.** Одинадцять фото згенеровано для цього шаблону в ChatGPT (OpenAI) і збережено у WebP, разом близько 1,2 МБ; промпти лежать у `img-prompts.json`. Люди й місця вигадані. Їх можна використовувати, але перед запуском замініть їх фото своєї клініки й команди.

**Медичні дані.** Ця форма лише для запиту на запис. Не збирайте через неї діагнози, історію хвороб, рецепти чи номери страховок; зберігайте це у власній системі клініки. Біля поля для коментаря є нагадування не писати медичних подробиць.

**Приклад змісту.** Відгуки, команда, ціни, план, адреси й телефон вигадані. Перед публікацією замініть їх своїми.

MIT license.
