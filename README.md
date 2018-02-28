# Ch2-ShowCurrentTime
Intro to Java Programming, Comprehensive Version, 10th Edition, Y. Daniel Liang

Question

        The problem is to develop a program that displays the current time in 
        GMT (Greenwich Mean Time) in the format hour:minute:second, such as 13:19:8.
        
Code

        public class ShowCurrentTime {

        public static void main (String args[]){

          //Obtain total milliseconds since midnight Jan 1, 1970
          long totalMilliseconds = System.currentTimeMillis();

          //obtain total seconds since date
          long totalSeconds = totalMilliseconds / 1000;

          //compute current second 
          long currentSecond = totalSeconds % 60;

          //obtain total minutes
          long totalMinutes = totalSeconds / 60;

          //compute current minute
          long currentMinute = totalMinutes % 60;

          //obtain total hours
          long totalHours = totalMinutes / 60;

          //compute current hour
          long currentHour = totalHours % 24;

          //dispay results
          System.out.println(currentHour + ":" + currentMinute +
              ":" + currentSecond + " GMT");
        }
      }
