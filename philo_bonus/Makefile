CC = cc
CFLAG = -Wall -Wextra -Werror
NAME = philosopher_bonus
HEAD = ./php.h
SRCS = srcs/main_bonus.c \
		srcs/process_bonus.c \
		srcs/src_bonus.c\
		srcs/src1_bonus.c \
		srcs/src2_bonus.c \
		srcs/src3_bonus.c \
		srcs/src4_bonus.c \
		srcs/thread1_bonus.c \
		srcs/action_bonus.c \
OBJS = $(SRCS:.c=.o)

all : $(NAME)

$(NAME) : $(OBJS) $(HAED)
	$(CC) $(CFLAG) -I $(HEAD) -o $(NAME) $(OBJS)

.c.o :
	$(CC) $(CFLAG) -I $(HEAD) -c $< -o $@

clean : 
	rm -rf *.o

fclean : clean
	rm -rf $(NAME)

re : fclean all

.PHONY : all re clean fclean
