---
layout: default
title: "ホーム"
description: "FFTPRS ワークショップの公式サイトへようこそ"
---

<!-- Hero Section -->
<section class="text-center mb-16">
    <div class="container mx-auto px-4 text-center">
        <h2 class="text-4xl font-bold text-gray-900 mb-4">有限体理論とその擬似乱数系列生成への応用ワークショップ</h2>
        <p class="text-lg text-gray-600 max-w-3xl mx-auto">サブタイトル（概要）</p>
    </div>
    
    <!-- アンカーリンク 
    <div class="flex justify-center mb-12">
        <nav class="flex flex-wrap gap-4 justify-center">
            <a href="#recent-workshops" class="inline-flex items-center px-4 py-2 bg-blue-600 text-white text-sm font-medium rounded-lg hover:bg-blue-700 transition-colors duration-200 shadow-sm">
                <svg class="w-4 h-4 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"></path>
                </svg>
                直近のワークショップ
            </a>
            <a href="#workshop-significance" class="inline-flex items-center px-4 py-2 bg-indigo-600 text-white text-sm font-medium rounded-lg hover:bg-indigo-700 transition-colors duration-200 shadow-sm">
                <svg class="w-4 h-4 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"></path>
                </svg>
                ワークショップの意義
            </a>
        </nav>
    </div>
    -->
</section>

<section class="mb-16" id="recent-workshops">
    <h3 class="text-3xl font-bold text-gray-800 mb-8 text-center">直近のFFTPRS ワークショップ</h3>
    <div class="grid md:grid-cols-2 lg:grid-cols-2 gap-8">
        {% assign sorted_workshops = site.data.workshops | where_exp: "item", "item.start_date != null" | sort: 'start_date' | reverse %}
        {% for workshop in sorted_workshops limit:2 %}
            <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow duration-300">
                <img alt="Workshop" class="w-full h-48 object-cover"
                    src="https://lh3.googleusercontent.com/aida-public/AB6AXuBu4B3SmV6I2BvvkQAlcXWOH1Bgt8qP2c4FNXqpCu9UVX6gelBUCtQfXnF_pmnqiIX4Og22kjdW2-hS7FOfAp3LseP5nbUjndZuJ-2lK4esOJC5IKved9fbQv-BkVv1Yqnbsrj21nlQHQmEb_lg04zRl8zsz5gxAmfcXJdX1qOr4zWkOqtIzbQ8zT6HiWUM_A7g4ADMJbtaaK1Rp4Bcu-XkQUQgbrPYMDksGfceZGdcwsKLLa4uNEVa9wpXGhyrnW-LGVkcKrx_Fd4" />
                <div class="p-6">
                    <h4 class="text-xl font-bold text-gray-800 mb-2">{{ workshop.title }}</h4>
                    <p class="text-sm text-gray-500 mb-4">{{ workshop.start_date | date: "%Y年%m月%d日" }} 〜 {{ workshop.end_date | date: "%Y年%m月%d日" }}</p>
                    <p class="text-sm text-gray-500 mb-4 font-bold">{{ workshop.status }}</p>
                    <p class="text-gray-700 mb-4">開催地: {{ workshop.location }}</p>
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
        <a href="/site/pages/workshops/" class="inline-flex items-center px-6 py-3 bg-green-600 text-white font-semibold rounded-lg hover:bg-green-700 transition-colors duration-300 shadow-md hover:shadow-lg">
            <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.746 0 3.332.477 4.5 1.253v13C19.832 18.477 18.246 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"></path>
            </svg>
            FFTPRS ワークショップ一覧を見る
        </a>
    </div>
</section>

<!-- About Section -->
<section class="bg-blue-50 rounded-lg p-8 md:p-12 mb-16" id="workshop-significance">
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
