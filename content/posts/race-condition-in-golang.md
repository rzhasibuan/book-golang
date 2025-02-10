---
date: '2025-02-10T10:08:00+07:00'
draft: false
title: 'Race condition in golang '
tags: ['golang', 'system design']
---


## race condition 
race condition adalah kondisi dimana dua atau lebih thread berusaha mangagkses data yang sama pada waktu berasamaan, dan salah satu dari thread tersebut melakukan write operation pada data tersebut
sehingga data tersebut menjadi tidak konsisten. 


