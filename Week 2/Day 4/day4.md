# Exercise 1 - (MongoDB)
# Install MongoDB and Mongo Compass
# How connect Mongo Compass to MongoDB
# Design Messaging and Notification System in MongoDB
# Messages Collection Will Documents, Every Document Will Have
# sender Sender info Like (id, name, etc..) and The Sender May Be Student Or Professor
# reciever Reciever info Like (id, name, etc..) and The Sender May Be Student Or Professor
# Notification Collection Will Documents, Every Document Will Have
# sender Sender info Like (id, name, etc..) and The Sender May Be Student Or Professor
# reciever Reciever info Like (id, name, etc..) and The Sender May Be Student Or Professor
# type Notification Type (Message For Now)
# content Notification Content
# is_read is Notification Read
# created_at Notification Creation Date
 
 # answer

# this command for Design Messaging and Notification System in MongoDB

# create database

- `use facebook`

# add anew data 

- `to db facebook`

# step 1
- `db.Messages.insert({ sender : {name : 'omar', id :1},receiver:{ name: 'fathy', id : 2},message:{ name : 'mohamed', id :3}})`

# step 2
- `db.Notification.insert({ sender : {name : 'ali', id :4},receiver:{ name: 'tamer', id : 5},type:{ type: 'string', id : 6},content:{ name: 'fady', id :    * 7},is_read:{ read: 'yes', id : 8},created_at:{date : '29/4/2022', id :10}})`

# 
