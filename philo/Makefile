SRCS		=	src/main.c src/parser.c src/logger.c src/time_utils.c src/philo.c

OBJS		=	${SRCS:.c=.o}

NAME		=	philo

CC			=	cc

CFLAGS		=	-pthread -Wall -Werror -Wextra -fsanitize=address

%.o: %.c
				$(CC) $(CFLAGS) -I./includes $< -c -o ${<:.c=.o}

all:			${NAME}

${NAME}:		${OBJS}
				${CC} ${CFLAGS} ${OBJS} -o ${NAME}
			
clean:
				rm -f ${OBJS} 

fclean:			clean
				rm -f ${NAME}

re:				fclean all

.PHONY:			all clean fclean re
