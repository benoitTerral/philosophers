# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: bterral <bterral@student.42.fr>            +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/03/07 11:30:47 by bterral           #+#    #+#              #
#    Updated: 2022/03/09 15:16:35 by bterral          ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME		= philo

SRCS		= actions.c monitoring.c parsing.c heap.c \
				philo.c time.c init.c

OBJS		= $(SRCS:.c=.o)

INCLUDES	= philo.h

CC			= gcc

CFLAGS		= -Wall -Wextra -Werror

RM			= rm -f

###### RULES ######

all: $(NAME)

$(NAME): $(OBJS)
	$(CC) $(CFLAGS) $(OBJS) -o $(NAME)

%.o: %.c $(INCLUDES) Makefile
	$(CC) $(CFLAGS) -I . -c $< -o $@

clean:
	$(RM) $(OBJS)

fclean: clean
	$(RM) $(NAME)

re: fclean all

.PHONY: all clean fclean re