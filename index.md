---
layout: default
title: "ホーム"
description: "FFTPRSWS ワークショップの公式サイトへようこそ"
---

<!-- Hero Section -->
<section class="text-center mb-16">
    <div class="container mx-auto px-4 text-center">
        <h2 class="text-4xl font-bold text-gray-900 mb-4">有限体理論とその擬似乱数系列生成への応用ワークショップ</h2>
        <p class="text-lg text-gray-600 max-w-3xl mx-auto">サブタイトル（概要）</p>
    </div>
</section>

<section class="mb-16">
    <h3 class="text-3xl font-bold text-gray-800 mb-8 text-center">開催予定のFFTPRSWS</h3>
    <div class="grid md:grid-cols-2 lg:grid-cols-2 gap-8">
        {% assign sorted_workshops = site.data.workshops | sort: 'start_date' | reverse %}
        {% for workshop in sorted_workshops limit:2 %}
            <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow duration-300">
                <img alt="Workshop" class="w-full h-48 object-cover"
                    src="https://lh3.googleusercontent.com/aida-public/AB6AXuBu4B3SmV6I2BvvkQAlcXWOH1Bgt8qP2c4FNXqpCu9UVX6gelBUCtQfXnF_pmnqiIX4Og22kjdW2-hS7FOfAp3LseP5nbUjndZuJ-2lK4esOJC5IKved9fbQv-BkVv1Yqnbsrj21nlQHQmEb_lg04zRl8zsz5gxAmfcXJdX1qOr4zWkOqtIzbQ8zT6HiWUM_A7g4ADMJbtaaK1Rp4Bcu-XkQUQgbrPYMDksGfceZGdcwsKLLa4uNEVa9wpXGhyrnW-LGVkcKrx_Fd4" />
                <div class="p-6">
                    <h4 class="text-xl font-bold text-gray-800 mb-2">{{ workshop.title }}</h4>
                    <p class="text-sm text-gray-500 mb-4">{{ workshop.start_date | date: "%Y年%m月%d日" }} 〜 {{ workshop.end_date | date: "%Y年%m月%d日" }}</p>
                    <p class="text-sm text-gray-500 mb-4 font-bold">{{ workshop.status }}</p>
                    <p class="text-gray-700 mb-4">{{ workshop.description }}</p>
                    {% if workshop.status == '未定' %}
                        <a class="inline-block bg-gray-300 text-gray-600 font-semibold px-6 py-2 rounded-lg cursor-not-allowed" href="#">詳細を見る</a>
                    {% else %}
                        <a class="inline-block bg-blue-600 text-white font-semibold px-6 py-2 rounded-lg hover:bg-blue-700 transition-colors duration-300" href="{{ workshop.url | relative_url }}">詳細を見る</a>
                    {% endif %}
                </div>
            </div>
        {% endfor %}
    </div>
    <div class="text-center mt-12">
        <a href="/site/pages/workshops/" class="btn-primary">
            過去のワークショップを見る
        </a>
    </div>
</section>

<!-- About Section -->
<section class="bg-blue-50 rounded-lg p-8 md:p-12 mb-16">
    <div class="flex flex-col md:flex-row items-center justify-between gap-8">
        <div class="md:w-1/2">
        <h3 class="text-3xl font-bold text-gray-800 mb-4">有限体理論とその擬似乱数系列生成への応用ワークショップの意義</h3>
        <p class="text-gray-700 leading-relaxed">私たちは、日頃より有限体理論やその擬似乱数系列生成への応用に関連する研究者、<br />
        またそのようなテーマに興味をもっている研究者が一堂に会し、日々の研究活動の中で得られた成果の報告をはじめ、疑問に思っている事柄、<br />
        あるいは個人的な興味から深く掘り下げているテーマなどを、十分な時間をかけてお互いに紹介し、共有し、密な議論を展開するための場を提供することを意図したワークショップです。
        それぞれの研究活動がより情熱をもって進められることへの一助になることを期待しています。</p>
    </div>
    <div class="md:w-1/2 flex justify-center">
        <div class="grid grid-cols-2 gap-4">
            <div class="bg-white p-6 rounded-lg shadow-md text-center">
                <span class="material-icons text-blue-600 text-4xl mb-2">school</span>
                <h4 class="font-bold text-gray-800">専門知識</h4>
                <p class="text-sm text-gray-600">各分野の研究者から学ぶ</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md text-center">
                <span class="material-icons text-blue-600 text-4xl mb-2">groups</span>
                <h4 class="font-bold text-gray-800">ネットワーキング</h4>
                <p class="text-sm text-gray-600">参加者同士の交流</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md text-center">
                <span class="material-icons text-blue-600 text-4xl mb-2">lightbulb</span>
                <h4 class="font-bold text-gray-800">インスピレーション</h4>
                <p class="text-sm text-gray-600">新たなアイデアの発見</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md text-center">
                <span class="material-icons text-blue-600 text-4xl mb-2">trending_up</span>
                <h4 class="font-bold text-gray-800">キャリア開発</h4>
                <p class="text-sm text-gray-600">スキルの向上</p>
            </div>
        </div>
    </div>
