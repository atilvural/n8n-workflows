create table reddit_post
(
    url       varchar(1000) charset utf8mb3 not null
        primary key,
    author    varchar(150) charset utf8mb3  null,
    title     text                          null,
    post      text                          null,
    ups       int                           null,
    downs     int                           null,
    processed bit default b'0'              null
);

create table saas_ideas
(
    id          int auto_increment
        primary key,
    category    varchar(255) charset utf8mb3  null,
    description text                          null,
    leads       varchar(2000) charset utf8mb3 null comment 'Comma separated usernames',
    posts       text                          null comment 'Comma separated post urls'
);

Required DB Schema
