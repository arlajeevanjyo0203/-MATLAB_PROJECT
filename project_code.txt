classdef memory_puzzle < matlab.apps.AppBase

    % Properties that correspond to app components
    properties (Access = public)
        UIFigure             matlab.ui.Figure
        TimeLabel            matlab.ui.control.Label
        SCOREEditField       matlab.ui.control.NumericEditField
        SCOREEditFieldLabel  matlab.ui.control.Label
        GIVEUPButton         matlab.ui.control.Button
        STARTButton          matlab.ui.control.Button
        Button_16            matlab.ui.control.Button
        Button_15            matlab.ui.control.Button
        Button_14            matlab.ui.control.Button
        Button_13            matlab.ui.control.Button
        Button_12            matlab.ui.control.Button
        Button_11            matlab.ui.control.Button
        Button_10            matlab.ui.control.Button
        Button_9             matlab.ui.control.Button
        Button_8             matlab.ui.control.Button
        Button_7             matlab.ui.control.Button
        Button_6             matlab.ui.control.Button
        Button_5             matlab.ui.control.Button
        Button_4             matlab.ui.control.Button
        Button_3             matlab.ui.control.Button
        Button_2             matlab.ui.control.Button
        Button_1             matlab.ui.control.Button
        MATCHITLabel         matlab.ui.control.Label
    end

    
    properties (Access = public)
        a;
        b;
        c;
        i;
        j=0;
        p=0;
        s=100;

        d;
        e;
        f;
        g;
        h;
        k;
        m;
        n;


   

        but1;
        but2;
        but3;
        but4;
        but5;
        but6;
        but7;
        but8;
        but9;
        but10;
        but11;
        but12;
        but13;
        but14;
        but15;
        but16;
        count = 0;
               

    end
    
    properties (Access = private)
        GameOver = false;
    end
    
    methods (Access = public)
        
        function results = func2(app)
            if(app.j==1)
                app.Button_1.Enable='off';
            elseif(app.j==2)
                app.Button_2.Enable='off';
            elseif(app.j==3)
                app.Button_3.Enable='off';
            elseif(app.j==4)
                app.Button_4.Enable='off';
            elseif(app.j==5)
                app.Button_5.Enable='off';
            elseif(app.j==6)
                app.Button_6.Enable='off';
            elseif(app.j==7)
                app.Button_7.Enable='off';
            elseif(app.j==8)
                app.Button_8.Enable='off';
            elseif(app.j==9)
                app.Button_9.Enable='off';
            elseif(app.j==10)
                app.Button_10.Enable='off';
            elseif(app.j==11)
                app.Button_11.Enable='off';
            elseif(app.j==12)
                app.Button_12.Enable='off';
            elseif(app.j==13)
                app.Button_13.Enable='off';
            elseif(app.j==14)
                app.Button_14.Enable='off';
            elseif(app.j==15)
                app.Button_15.Enable='off';
            else
                app.Button_16.Enable='off';
            end
            
            
       end
        
        function results = func3(app)
            if(app.j==1)
                app.Button_1.Icon='';
            elseif(app.j==2)
                app.Button_2.Icon='';
            elseif(app.j==3)
                app.Button_3.Icon='';
            elseif(app.j==4)
                app.Button_4.Icon='';  
            elseif(app.j==5)
                app.Button_5.Icon='';
            elseif(app.j==6)
                app.Button_6.Icon='';
            elseif(app.j==7)
                app.Button_7.Icon='';
            elseif(app.j==8)
                app.Button_8.Icon='';
            elseif(app.j==9)
                app.Button_9.Icon='';
            elseif(app.j==10)
                app.Button_10.Icon='';
            elseif(app.j==11)
                app.Button_11.Icon='';
            elseif(app.j==12)
                app.Button_12.Icon='';
            elseif(app.j==13)
                app.Button_13.Icon='';
            elseif(app.j==14)
                app.Button_14.Icon='';
            elseif(app.j==15)
                app.Button_15.Icon='';
            else
                app.Button_16.Icon='';
            
            end
        end
        
        function results = func(app)
            app.SCOREEditField.Value=app.s;
            app.d=datetime('12:03:00','Format','hh:mm:ss');
            app.e=datetime('12:04:00','Format','hh:mm:ss');
            app.f=app.e-app.d;
            app.h=datetime('now','Format','hh:mm:ss');
            app.k=app.h-app.g;
            app.m=app.k-app.f;
            app.n=string(app.m);
            app.TimeLabel.Text=app.n;


                    
            if (app.s<=0)
                msgbox('sorry you were  out of moves,please try again')

            app.Button_1.Icon=app.but1;
            app.Button_2.Icon=app.but2;
            app.Button_3.Icon=app.but3;
            app.Button_4.Icon=app.but4;
            app.Button_5.Icon=app.but5;
            app.Button_6.Icon=app.but6;
            app.Button_7.Icon=app.but7;
            app.Button_8.Icon=app.but8;
            app.Button_9.Icon=app.but9;
            app.Button_10.Icon=app.but10;
            app.Button_11.Icon=app.but11;
            app.Button_12.Icon=app.but12;
            app.Button_13.Icon=app.but13;
            app.Button_14.Icon=app.but14;
            app.Button_15.Icon=app.but15;
            app.Button_16.Icon=app.but16;

            app.Button_1.Enable="off";
            app.Button_2.Enable="off";
            app.Button_3.Enable="off";
            app.Button_4.Enable="off";
            app.Button_5.Enable="off";
            app.Button_6.Enable="off";
            app.Button_7.Enable="off";
            app.Button_8.Enable="off";
            app.Button_9.Enable="off";
            app.Button_10.Enable="off";
            app.Button_11.Enable="off";
            app.Button_12.Enable="off";
            app.Button_13.Enable="off";
            app.Button_14.Enable="off";
            app.Button_15.Enable="off";
            app.Button_16.Enable="off";

            app.GIVEUPButton.Enable='off';
            app.STARTButton.Enable='on';
            
            
            app.SCOREEditField.Value=0;

            app.p=0;
            elseif(app.k>app.f)
                msgbox('sorry,you are out of time');
            elseif(app.SCOREEditField.Value==50);
                msgbox("Game Over");

                app.Button_1.Enable="off";
                app.Button_2.Enable="off";
                app.Button_3.Enable="off";
                app.Button_4.Enable="off";
                app.Button_5.Enable="off";
                app.Button_6.Enable="off";
                app.Button_7.Enable="off";
                app.Button_8.Enable="off";
                app.Button_9.Enable="off";
                app.Button_10.Enable="off";
                app.Button_11.Enable="off";
                app.Button_12.Enable="off";
                app.Button_13.Enable="off";
                app.Button_14.Enable="off";
                app.Button_15.Enable="off";
                app.Button_16.Enable="off";

                app.GameOver = true
                
            end

            if(app.p==8)
                msgbox('Hurray! you have won the game');
                app.p=0;
                app.STARTButton.Enable='on';

            
        end
    end
 end 

    % Callbacks that handle component events
    methods (Access = private)

        % Button pushed function: STARTButton
        function STARTButtonPushed(app, event)
               
            app.a=[1:8 1:8];
            app.b=randperm(16);
            app.c=app.a(app.b(1:16));
            app.d=datetime('12:03:00','Format','hh:mm:ss');
            app.e=datetime('12:04:00','Format','hh:mm:ss');
            app.f=app.e-app.d;
            app.m=string(app.f);
            app.TimeLabel.Text=app.m;
            app.g=datetime('now','Format','hh,mm,ss');
                       
            if(app.c(1)==1)
                app.Button_1.Icon='1.jpeg';
                app.but1='1.jpeg';
            elseif(app.c(1)==2)
                app.Button_1.Icon='2.jpeg';
                app.but1='2.jpeg';
            elseif(app.c(1)==3)
                app.Button_1.Icon='3.jpeg';
                app.but1='3.jpeg';
            elseif(app.c(1)==4)
                app.Button_1.Icon='4.jpeg';
                app.but1='4.jpeg';
            elseif(app.c(1)==5)
                app.Button_1.Icon='5.jpeg';
                app.but1='5.jpeg';
            elseif(app.c(1)==6)
                app.Button_1.Icon='6.jpeg';
                app.but1='6.jpeg';
            elseif(app.c(1)==7)
                app.Button_1.Icon='7.jpeg';
                app.but1='7.jpeg';
            else
                app.Button_1.Icon='9.jpeg';
                app.but1='9.jpeg';
            end
            

            if(app.c(2)==1)
                app.Button_2.Icon='1.jpeg';
                app.but2='1.jpeg';
            elseif(app.c(2)==2)
                app.Button_2.Icon='2.jpeg';
                app.but2='2.jpeg';
            elseif(app.c(2)==3)
                app.Button_2.Icon='3.jpeg';
                app.but2='3.jpeg';
            elseif(app.c(2)==4)
                app.Button_2.Icon='4.jpeg';
                app.but2='4.jpeg';
            elseif(app.c(2)==5)
                app.Button_2.Icon='5.jpeg';
                app.but2='5.jpeg';
            elseif(app.c(2)==6)
                app.Button_2.Icon='6.jpeg';
                app.but2='6.jpeg';
            elseif(app.c(2)==7)
                app.Button_2.Icon='7.jpeg';
                app.but2='7.jpeg';
            else
                app.Button_2.Icon='9.jpeg';
                app.but2='9.jpeg';
            end
            

            if(app.c(3)==1)
                app.Button_3.Icon='1.jpeg';
                app.but3='1.jpeg';
            elseif(app.c(3)==2)
                app.Button_3.Icon='2.jpeg';
                app.but3='2.jpeg';
            elseif(app.c(3)==3)
                app.Button_3.Icon='3.jpeg';
                app.but3='3.jpeg';
            elseif(app.c(3)==4)
                app.Button_3.Icon='4.jpeg';
                app.but3='4.jpeg';
            elseif(app.c(3)==5)
                app.Button_3.Icon='5.jpeg';
                app.but3='5.jpeg';
            elseif(app.c(3)==6)
                app.Button_3.Icon='6.jpeg';
                app.but3='6.jpeg';
            elseif(app.c(3)==7)
                app.Button_3.Icon='7.jpeg';
                app.but3='7.jpeg';
            else
                app.Button_3.Icon='9.jpeg';
                app.but3='9.jpeg';
            end

            if(app.c(4)==1)
                app.Button_4.Icon='1.jpeg';
                app.but4='1.jpeg';
            elseif(app.c(4)==2)
                app.Button_4.Icon='2.jpeg';
                app.but4='2.jpeg';
            elseif(app.c(4)==3)
                app.Button_4.Icon='3.jpeg';
                app.but4='3.jpeg';
            elseif(app.c(4)==4)
                app.Button_4.Icon='4.jpeg';
                app.but4='4.jpeg';
            elseif(app.c(4)==5)
                app.Button_4.Icon='5.jpeg';
                app.but4='5.jpeg';
            elseif(app.c(4)==6)
                app.Button_4.Icon='6.jpeg';
                app.but4='6.jpeg';
            elseif(app.c(4)==7)
                app.Button_4.Icon='7.jpeg';
                app.but4='7.jpeg';
            else
                app.Button_4.Icon='9.jpeg';
                app.but4='9.jpeg';
            end

            if(app.c(5)==1)
                app.Button_5.Icon='1.jpeg';
                app.but5='1.jpeg';
            elseif(app.c(5)==2)
                app.Button_5.Icon='2.jpeg';
                app.but5='2.jpeg';
            elseif(app.c(5)==3)
                app.Button_5.Icon='3.jpeg';
                app.but5='3.jpeg';
            elseif(app.c(5)==4)
                app.Button_5.Icon='4.jpeg';
                app.but5='4.jpeg';
            elseif(app.c(5)==5)
                app.Button_5.Icon='5.jpeg';
                app.but5='5.jpeg';
            elseif(app.c(5)==6)
                app.Button_5.Icon='6.jpeg';
                app.but5='6.jpg';
            elseif(app.c(5)==7)
                app.Button_5.Icon='7.jpg';
                app.but5='7.jpeg';
            else
                app.Button_5.Icon='9.jpeg';
                app.but5='9.jpeg';
            end


            if(app.c(6)==1)
                app.Button_6.Icon='1.jpeg';
                app.but6='1.jpeg';
            elseif(app.c(6)==2)
                app.Button_6.Icon='2.jpeg';
                app.but6='2.jpeg';
            elseif(app.c(6)==3)
                app.Button_6.Icon='3.jpeg';
                app.but6='3.jpeg';
            elseif(app.c(6)==4)
                app.Button_6.Icon='4.jpeg';
                app.but6='4.jpeg';
            elseif(app.c(6)==5)
                app.Button_6.Icon='5.jpeg';
                app.but6='5.jpeg';
            elseif(app.c(6)==6)
                app.Button_6.Icon='6.jpeg';
                app.but6='6.jpeg';
            elseif(app.c(6)==7)
                app.Button_6.Icon='7.jpeg';
                app.but6='7.jpeg';
            else
                app.Button_6.Icon='9.jpeg';
                app.but6='9.jpeg';
            end


            if(app.c(7)==1)
                app.Button_7.Icon='1.jpeg';
                app.but7='1.jpeg';
            elseif(app.c(7)==2)
                app.Button_7.Icon='2.jpeg';
                app.but7='2.jpeg';
            elseif(app.c(7)==3)
                app.Button_7.Icon='3.jpeg';
                app.but7='3.jpeg';
            elseif(app.c(7)==4)
                app.Button_7.Icon='4.jpeg';
                app.but7='4.jpg';
            elseif(app.c(7)==5)
                app.Button_7.Icon='5.jpg';
                app.but7='5.jpeg';
            elseif(app.c(7)==6)
                app.Button_7.Icon='6.jpeg';
                app.but7='6.jpeg';
            elseif(app.c(7)==7)
                app.Button_7.Icon='7.jpeg';
                app.but7='7.jpeg';
            else
                app.Button_7.Icon='9.jpeg';
                app.but7='9.jpeg';
            end


            if(app.c(8)==1)
                app.Button_8.Icon='1.jpeg';
                app.but8='1.jpeg';
            elseif(app.c(8)==2)
                app.Button_8.Icon='2.jpeg';
                app.but8='2.jpeg';
            elseif(app.c(8)==3)
                app.Button_8.Icon='3.jpeg';
                app.but8='3.jpeg';
            elseif(app.c(8)==4)
                app.Button_8.Icon='4.jpeg';
                app.but8='4.jpeg';
            elseif(app.c(8)==5)
                app.Button_8.Icon='5.jpeg';
                app.but8='5.jpeg';
            elseif(app.c(8)==6)
                app.Button_8.Icon='6.jpeg';
                app.but8='6.jpeg';
            elseif(app.c(8)==7)
                app.Button_8.Icon='7.jpeg';
                app.but8='7.jpeg';
            else
                app.Button_8.Icon='9.jpeg';
                app.but8='9.jpeg';
            end

            if(app.c(9)==1)
                app.Button_9.Icon='1.jpeg';
                app.but9='1.jpeg';
            elseif(app.c(9)==2)
                app.Button_9.Icon='2.jpeg';
                app.but9='2.jpeg';
            elseif(app.c(9)==3)
                app.Button_9.Icon='3.jpeg';
                app.but9='3.jpeg';
            elseif(app.c(9)==4)
                app.Button_9.Icon='4.jpeg';
                app.but9='4.jpeg';
            elseif(app.c(9)==5)
                app.Button_9.Icon='5.jpeg';
                app.but9='5.jpeg';
            elseif(app.c(9)==6)
                app.Button_9.Icon='6.jpeg';
                app.but9='6.jpeg';
            elseif(app.c(9)==7)
                app.Button_9.Icon='7.jpeg';
                app.but9='7.jpeg';
            else
                app.Button_9.Icon='9.jpeg';
                app.but9='9.jpeg';
            end


            if(app.c(10)==1)
                app.Button_10.Icon='1.jpeg';
                app.but10='1.jpeg';
            elseif(app.c(10)==2)
                app.Button_10.Icon='2.jpeg';
                app.but10='2.jpeg';
            elseif(app.c(10)==3)
                app.Button_10.Icon='3.jpeg';
                app.but10='3.jpeg';
            elseif(app.c(10)==4)
                app.Button_10.Icon='4.jpeg';
                app.but10='4.jpeg';
            elseif(app.c(10)==5)
                app.Button_10.Icon='5.jpeg';
                app.but10='5.jpeg';
            elseif(app.c(10)==6)
                app.Button_10.Icon='6.jpeg';
                app.but10='6.jpeg';
            elseif(app.c(10)==7)
                app.Button_10.Icon='7.jpeg';
                app.but10='7.jpeg';
            else
                app.Button_10.Icon='9.jpeg';
                app.but10='9.jpeg';
            end


            if(app.c(11)==1)
                app.Button_11.Icon='1.jpeg';
                app.but11='1.jpeg';
            elseif(app.c(11)==2)
                app.Button_11.Icon='2.jpeg';
                app.but11='2.jpeg';
            elseif(app.c(11)==3)
                app.Button_11.Icon='3.jpeg';
                app.but11='3.jpeg';
            elseif(app.c(11)==4)
                app.Button_11.Icon='4.jpeg';
                app.but11='4.jpeg';
            elseif(app.c(11)==5)
                app.Button_11.Icon='5.jpeg';
                app.but11='5.jpeg';
            elseif(app.c(11)==6)
                app.Button_11.Icon='6.jpeg';
                app.but11='6.jpeg';
            elseif(app.c(11)==7)
                app.Button_11.Icon='7.jpeg';
                app.but11='7.jpeg';
            else
                app.Button_11.Icon='9.jpeg';
                app.but11='9.jpeg';
            end



            if(app.c(12)==1)
                app.Button_12.Icon='1.jpeg';
                app.but12='1.jpeg';
            elseif(app.c(12)==2)
                app.Button_12.Icon='2.jpeg';
                app.but12='2.jpeg';
            elseif(app.c(12)==3)
                app.Button_12.Icon='3.jpeg';
                app.but12='3.jpeg';
            elseif(app.c(12)==4)
                app.Button_12.Icon='4.jpeg';
                app.but12='4.jpeg';
            elseif(app.c(12)==5)
                app.Button_12.Icon='5.jpeg';
                app.but12='5.jpeg';
            elseif(app.c(12)==6)
                app.Button_12.Icon='6.jpeg';
                app.but12='6.jpeg';
            elseif(app.c(12)==7)
                app.Button_12.Icon='7.jpeg';
                app.but12='7.jpeg';
            else
                app.Button_12.Icon='9.jpeg';
                app.but12='9.jpeg';
            end



           if(app.c(13)==1)
                app.Button_13.Icon='1.jpeg';
                app.but13='1.jpeg';
            elseif(app.c(13)==2)
                app.Button_13.Icon='2.jpeg';
                app.but13='2.jpeg';
            elseif(app.c(13)==3)
                app.Button_13.Icon='3.jpeg';
                app.but13='3.jpeg';
            elseif(app.c(13)==4)
                app.Button_13.Icon='4.jpeg';
                app.but13='4.jpeg';
            elseif(app.c(13)==5)
                app.Button_13.Icon='5.jpeg';
                app.but13='5.jpeg';
            elseif(app.c(13)==6)
                app.Button_13.Icon='6.jpeg';
                app.but13='6.jpeg';
            elseif(app.c(13)==7)
                app.Button_13.Icon='7.jpeg';
                app.but13='7.jpeg';
            else
                app.Button_13.Icon='9.jpeg';
                app.but13='9.jpeg';
            end



             if(app.c(14)==1)
                app.Button_14.Icon='1.jpeg';
                app.but14='1.jpeg';
            elseif(app.c(14)==2)
                app.Button_14.Icon='2.jpeg';
                app.but14='2.jpeg';
            elseif(app.c(14)==3)
                app.Button_14.Icon='3.jpeg';
                app.but14='3.jpeg';
            elseif(app.c(14)==4)
                app.Button_14.Icon='4.jpeg';
                app.but14='4.jpeg';
            elseif(app.c(14)==5)
                app.Button_14.Icon='5.jpeg';
                app.but14='5.jpeg';
            elseif(app.c(14)==6)
                app.Button_14.Icon='6.jpeg';
                app.but14='6.jpeg';
            elseif(app.c(14)==7)
                app.Button_14.Icon='7.jpeg';
                app.but14='7.jpeg';
            else
                app.Button_14.Icon='9.jpeg';
                app.but14='9.jpeg';
            end


            if(app.c(15)==1)
                app.Button_15.Icon='1.jpeg';
                app.but15='1.jpeg';
            elseif(app.c(15)==2)
                app.Button_15.Icon='2.jpeg';
                app.but15='2.jpeg';
            elseif(app.c(15)==3)
                app.Button_15.Icon='3.jpeg';
                app.but15='3.jpeg';
            elseif(app.c(15)==4)
                app.Button_15.Icon='4.jpeg';
                app.but15='4.jpeg';
            elseif(app.c(15)==5)
                app.Button_15.Icon='5.jpeg';
                app.but15='5.jpeg';
            elseif(app.c(15)==6)
                app.Button_15.Icon='6.jpeg';
                app.but15='6.jpeg';
            elseif(app.c(15)==7)
                app.Button_15.Icon='7.jpeg';
                app.but15='7.jpeg';
            else
                app.Button_15.Icon='9.jpeg';
                app.but15='9.jpeg';
            end



            if(app.c(16)==1)
                app.Button_16.Icon='1.jpeg';
                app.but16='1.jpeg';
            elseif(app.c(16)==2)
                app.Button_16.Icon='2.jpeg';
                app.but16='2.jpeg';
            elseif(app.c(16)==3)
                app.Button_16.Icon='3.jpeg';
                app.but16='3.jpeg';
            elseif(app.c(16)==4)
                app.Button_16.Icon='4.jpeg';
                app.but16='4.jpeg';
            elseif(app.c(16)==5)
                app.Button_16.Icon='5.jpeg';
                app.but16='5.jpeg';
            elseif(app.c(16)==6)
                app.Button_16.Icon='6.jpeg';
                app.but16='6.jpeg';
            elseif(app.c(16)==7)
                app.Button_16.Icon='7.jpeg';
                app.but16='7.jpeg';
            else
                app.Button_16.Icon='9.jpeg';
                app.but16='9.jpeg';
            end
            pause(3);
            app.Button_1.Icon='';
            app.Button_2.Icon='';
            app.Button_3.Icon='';
            app.Button_4.Icon='';
            app.Button_5.Icon='';
            app.Button_6.Icon='';
            app.Button_7.Icon='';
            app.Button_8.Icon='';
            app.Button_9.Icon='';
            app.Button_10.Icon='';
            app.Button_11.Icon='';
            app.Button_12.Icon='';
            app.Button_12.Icon='';
            app.Button_13.Icon='';
            app.Button_14.Icon='';
            app.Button_15.Icon='';
            app.Button_16.Icon='';


            app.Button_1.Enable='on';
            app.Button_2.Enable='on';
            app.Button_3.Enable='on';
            app.Button_4.Enable='on';
            app.Button_5.Enable='on';
            app.Button_6.Enable='on';
            app.Button_7.Enable='on';
            app.Button_8.Enable='on';
            app.Button_9.Enable='on';
            app.Button_10.Enable='on';
            app.Button_11.Enable='on';
            app.Button_12.Enable='on';
            app.Button_12.Enable='on';
            app.Button_13.Enable='on';
            app.Button_14.Enable='on';
            app.Button_15.Enable='on';
            app.Button_16.Enable='on';


            app.STARTButton.Text='RESTART';
            app.GIVEUPButton.Enable="on";
            

        end

        % Button pushed function: Button_1
        function Button_1Pushed(app, event)
      if app.GameOver
          return;
      end
       if(app.j~=1)
            app.Button_1.Icon=app.but1;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(1)==app.i)
                    app.Button_1.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(1);
                    app.j=1;
                    app.count=app.count-1;
                    app.s=app.s-5;
                end   
          

            else
                app.i=app.c(1);
                app.j=1 ;

            end
      end
      func(app);
        end

        % Button pushed function: Button_2
        function Button_2Pushed(app, event)
      if app.GameOver
          return;
      end
      if(app.j~=2)
            app.Button_2.Icon=app.but2;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(2)==app.i)
                    app.Button_2.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(2);
                    app.j=2;
                    app.count=app.count-1;
                    app.s=app.s-5;
                end   
          

            else
                app.i=app.c(2);
                app.j=2 ;

            end
      end
      func(app);
        end

        % Button pushed function: Button_3
        function Button_3Pushed(app, event)
      if app.GameOver
          return;
      end
       if(app.j~=3)
            app.Button_3.Icon=app.but3;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(3)==app.i)
                    app.Button_3.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(3);
                    app.j=3;
                    app.count=app.count-1;
                    app.s=app.s-5;

                end   
          

            else
                app.i=app.c(3);
                app.j=3 ;

            end
      end
       func(app);
        end

        % Button pushed function: Button_4
        function Button_4Pushed(app, event)
      if app.GameOver
          return;
      end
       if(app.j~=4)
            app.Button_4.Icon=app.but4;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(4)==app.i)
                    app.Button_4.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(4);
                    app.j=4;
                    app.count=app.count-1;
                    app.s=app.s-5;

                end   
          

            else
                app.i=app.c(4);
                app.j=4 ;

            end
      end
       func(app);
        end

        % Button pushed function: Button_5
        function Button_5Pushed(app, event)
      if app.GameOver
          return;
      end
      if(app.j~=5)
            app.Button_5.Icon=app.but5;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(5)==app.i)
                    app.Button_5.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(5);
                    app.j=5;
                    app.count=app.count-1;
                    app.s=app.s-5;

                end   
          

            else
                % % app.i=app.c(5);
                app.j=5 ;

            end
     end
      func(app);
        end

        % Button pushed function: Button_6
        function Button_6Pushed(app, event)
     if app.GameOver
          return;
      end
      if(app.j~=6)
            app.Button_6.Icon=app.but6;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(6)==app.i)
                    app.Button_6.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(6);
                    app.j=6;
                    app.count=app.count-1;
                    app.s=app.s-5;

                end   
          

            else
                app.i=app.c(6);
                app.j=6 ;

            end
     end
      func(app);
        end

        % Button pushed function: Button_7
        function Button_7Pushed(app, event)
     if app.GameOver
          return;
      end
      if(app.j~=7)
            app.Button_7.Icon=app.but7;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(7)==app.i)
                    app.Button_7.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(7);
                    app.j=7;
                    app.count=app.count-1;
                    app.s=app.s-5;

                end   
          

            else
                app.i=app.c(7);
                app.j=7 ;

            end
     end
      func(app);
        end

        % Button pushed function: Button_8
        function Button_8Pushed(app, event)
      if app.GameOver
          return;
      end
      if(app.j~=8)
            app.Button_8.Icon=app.but8;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(8)==app.i)
                    app.Button_8.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(8);
                    app.j=8;
                    app.count=app.count-1;
                    app.s=app.s-5;


                end   
          

            else
                app.i=app.c(8);
                app.j=8 ;

            end
      end
       func(app);
        end

        % Button pushed function: Button_9
        function Button_9Pushed(app, event)
      if app.GameOver
          return;
      end
       if(app.j~=9)
            app.Button_9.Icon=app.but9;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(9)==app.i)
                    app.Button_9.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(9);
                    app.j=9;
                    app.count=app.count-1;
                    app.s=app.s-5;

                end   
          

            else
                app.i=app.c(9);
                app.j=9 ;

            end
      end
       func(app);
        end

        % Button pushed function: Button_10
        function Button_10Pushed(app, event)
      if app.GameOver
          return;
      end
       if(app.j~=10)
            app.Button_10.Icon=app.but10;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(10)==app.i)
                    app.Button_10.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(10);
                    app.j=10;
                    app.count=app.count-1;
                    app.s=app.s-5;

                end   
          

            else
                app.i=app.c(10);
                app.j=10 ;

            end
      end
       func(app);
        end

        % Button pushed function: Button_11
        function Button_11Pushed(app, event)
      if app.GameOver
          return;
      end
       if(app.j~=11)
            app.Button_11.Icon=app.but11;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(11)==app.i)
                    app.Button_11.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(11);
                    app.j=11;
                    app.count=app.count-1;
                    app.s=app.s-5;

                end   
          

            else
                app.i=app.c(11);
                app.j=11 ;

            end
      end
       func(app);

        end

        % Button pushed function: Button_13
        function Button_13Pushed(app, event)
      if app.GameOver
          return;
      end
      if(app.j~=13)
            app.Button_13.Icon=app.but13;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(13)==app.i)
                    app.Button_13.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(13);
                    app.j=13;
                    app.count=app.count-1;
                    app.s=app.s-5;

                end   
          

            else
                app.i=app.c(13);
                app.j=13 ;

            end
      end
       func(app);
        end

        % Button pushed function: Button_14
        function Button_14Pushed(app, event)
      if app.GameOver
          return;
      end
      if(app.j~=14)
            app.Button_14.Icon=app.but14;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(14)==app.i)
                    app.Button_14.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(14);
                    app.j=14;
                    app.count=app.count-1;
                    app.s=app.s-5;

                end   
          

            else
                app.i=app.c(14);
                app.j=14 ;

            end
      end
       func(app);
        end

        % Button pushed function: Button_15
        function Button_15Pushed(app, event)
      if app.GameOver
          return;
      end
       if(app.j~=15)
            app.Button_15.Icon=app.but15;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(15)==app.i)
                    app.Button_15.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(15);
                    app.j=15;
                    app.count=app.count-1;
                    app.s=app.s-5;

                end   
          

            else
                app.i=app.c(15);
                app.j=15 ;

            end
      end
       func(app);
        end

        % Button pushed function: Button_16
        function Button_16Pushed(app, event)
      if app.GameOver
          return;
      end
      if(app.j~=16)
            app.Button_16.Icon=app.but16;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(16)==app.i)
                    app.Button_16.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(16);
                    app.j=16;
                    app.count=app.count-1;
                    app.s=app.s-5;

                end   
          

            else
                app.i=app.c(16);
                app.j=16;

            end
      end
       func(app);
        end

        % Button pushed function: GIVEUPButton
        function GIVEUPButtonPushed(app, event)
            app.Button_1.Icon=app.but1;
            app.Button_2.Icon=app.but2;
            app.Button_3.Icon=app.but3;
            app.Button_4.Icon=app.but4;
            app.Button_5.Icon=app.but5;
            app.Button_6.Icon=app.but6;
            app.Button_7.Icon=app.but7;
            app.Button_8.Icon=app.but8;
            app.Button_9.Icon=app.but9;
            app.Button_10.Icon=app.but10;
            app.Button_11.Icon=app.but11;
            app.Button_12.Icon=app.but12;
            app.Button_13.Icon=app.but13;
            app.Button_14.Icon=app.but14;
            app.Button_15.Icon=app.but15;
            app.Button_16.Icon=app.but16;

            app.Button_1.Enable="off";
            app.Button_2.Enable="off";
            app.Button_3.Enable="off";
            app.Button_4.Enable="off";
            app.Button_5.Enable="off";
            app.Button_6.Enable="off";
            app.Button_7.Enable="off";
            app.Button_8.Enable="off";
            app.Button_9.Enable="off";
            app.Button_10.Enable="off";
            app.Button_11.Enable="off";
            app.Button_12.Enable="off";
            app.Button_13.Enable="off";
            app.Button_14.Enable="off";
            app.Button_15.Enable="off";
            app.Button_16.Enable="off";

            app.GIVEUPButton.Enable='off';
            app.STARTButton.Enable='on';

            msgbox('sorry,better luck next time');
            app.SCOREEditField.Value=0;
            app.p=0;


        end

        % Button pushed function: Button_12
        function Button_12Pushed(app, event)
            if(app.j~=12)
            app.Button_12.Icon=app.but12;
            app.count=app.count+1;
            if(app.count==2)
                if (app.c(12)==app.i)
                    app.Button_12.Enable='off';
                    app.p=app.p+1
                    func2(app);
                    app.count=0;
                else
                    func3(app);
                    app.i=app.c(12);
                    app.j=12;
                    app.count=app.count-1;
                    app.s=app.s-5;

                end   
          

            else
                app.i=app.c(12);
                app.j=12;

            end
      end
       func(app);
        end
    end

    % Component initialization
    methods (Access = private)

        % Create UIFigure and components
        function createComponents(app)

            % Create UIFigure and hide until all components are created
            app.UIFigure = uifigure('Visible', 'off');
            app.UIFigure.Color = [0 0 0];
            app.UIFigure.Position = [100.2 100.2 640 480];
            app.UIFigure.Name = 'MATLAB App';

            % Create MATCHITLabel
            app.MATCHITLabel = uilabel(app.UIFigure);
            app.MATCHITLabel.BackgroundColor = [1 0.0745 0.651];
            app.MATCHITLabel.FontSize = 36;
            app.MATCHITLabel.FontWeight = 'bold';
            app.MATCHITLabel.Position = [193 407 174 47];
            app.MATCHITLabel.Text = 'MATCH IT';

            % Create Button_1
            app.Button_1 = uibutton(app.UIFigure, 'push');
            app.Button_1.ButtonPushedFcn = createCallbackFcn(app, @Button_1Pushed, true);
            app.Button_1.BackgroundColor = [0.8 0.8 0.8];
            app.Button_1.Position = [92 332 89 62];
            app.Button_1.Text = '';

            % Create Button_2
            app.Button_2 = uibutton(app.UIFigure, 'push');
            app.Button_2.ButtonPushedFcn = createCallbackFcn(app, @Button_2Pushed, true);
            app.Button_2.BackgroundColor = [0.8 0.8 0.8];
            app.Button_2.FontSize = 18;
            app.Button_2.Position = [92 239 89 62];
            app.Button_2.Text = '';

            % Create Button_3
            app.Button_3 = uibutton(app.UIFigure, 'push');
            app.Button_3.ButtonPushedFcn = createCallbackFcn(app, @Button_3Pushed, true);
            app.Button_3.BackgroundColor = [0.8 0.8 0.8];
            app.Button_3.Position = [92 151 89 62];
            app.Button_3.Text = '';

            % Create Button_4
            app.Button_4 = uibutton(app.UIFigure, 'push');
            app.Button_4.ButtonPushedFcn = createCallbackFcn(app, @Button_4Pushed, true);
            app.Button_4.BackgroundColor = [0.8 0.8 0.8];
            app.Button_4.Position = [92 61 89 62];
            app.Button_4.Text = '';

            % Create Button_5
            app.Button_5 = uibutton(app.UIFigure, 'push');
            app.Button_5.ButtonPushedFcn = createCallbackFcn(app, @Button_5Pushed, true);
            app.Button_5.BackgroundColor = [0.8 0.8 0.8];
            app.Button_5.Position = [230 332 89 62];
            app.Button_5.Text = '';

            % Create Button_6
            app.Button_6 = uibutton(app.UIFigure, 'push');
            app.Button_6.ButtonPushedFcn = createCallbackFcn(app, @Button_6Pushed, true);
            app.Button_6.BackgroundColor = [0.8 0.8 0.8];
            app.Button_6.Position = [230 239 89 62];
            app.Button_6.Text = '';

            % Create Button_7
            app.Button_7 = uibutton(app.UIFigure, 'push');
            app.Button_7.ButtonPushedFcn = createCallbackFcn(app, @Button_7Pushed, true);
            app.Button_7.BackgroundColor = [0.8 0.8 0.8];
            app.Button_7.Position = [230 151 89 62];
            app.Button_7.Text = '';

            % Create Button_8
            app.Button_8 = uibutton(app.UIFigure, 'push');
            app.Button_8.ButtonPushedFcn = createCallbackFcn(app, @Button_8Pushed, true);
            app.Button_8.BackgroundColor = [0.8 0.8 0.8];
            app.Button_8.Position = [230 61 89 62];
            app.Button_8.Text = '';

            % Create Button_9
            app.Button_9 = uibutton(app.UIFigure, 'push');
            app.Button_9.ButtonPushedFcn = createCallbackFcn(app, @Button_9Pushed, true);
            app.Button_9.BackgroundColor = [0.8 0.8 0.8];
            app.Button_9.Position = [366 332 89 62];
            app.Button_9.Text = '';

            % Create Button_10
            app.Button_10 = uibutton(app.UIFigure, 'push');
            app.Button_10.ButtonPushedFcn = createCallbackFcn(app, @Button_10Pushed, true);
            app.Button_10.BackgroundColor = [0.8 0.8 0.8];
            app.Button_10.Position = [366 239 89 62];
            app.Button_10.Text = '';

            % Create Button_11
            app.Button_11 = uibutton(app.UIFigure, 'push');
            app.Button_11.ButtonPushedFcn = createCallbackFcn(app, @Button_11Pushed, true);
            app.Button_11.BackgroundColor = [0.8 0.8 0.8];
            app.Button_11.Position = [366 151 89 62];
            app.Button_11.Text = '';

            % Create Button_12
            app.Button_12 = uibutton(app.UIFigure, 'push');
            app.Button_12.ButtonPushedFcn = createCallbackFcn(app, @Button_12Pushed, true);
            app.Button_12.BackgroundColor = [0.8 0.8 0.8];
            app.Button_12.Position = [366 61 89 62];
            app.Button_12.Text = '';

            % Create Button_13
            app.Button_13 = uibutton(app.UIFigure, 'push');
            app.Button_13.ButtonPushedFcn = createCallbackFcn(app, @Button_13Pushed, true);
            app.Button_13.BackgroundColor = [0.8 0.8 0.8];
            app.Button_13.Position = [503 332 89 62];
            app.Button_13.Text = '';

            % Create Button_14
            app.Button_14 = uibutton(app.UIFigure, 'push');
            app.Button_14.ButtonPushedFcn = createCallbackFcn(app, @Button_14Pushed, true);
            app.Button_14.BackgroundColor = [0.8 0.8 0.8];
            app.Button_14.Position = [503 151 89 62];
            app.Button_14.Text = '';

            % Create Button_15
            app.Button_15 = uibutton(app.UIFigure, 'push');
            app.Button_15.ButtonPushedFcn = createCallbackFcn(app, @Button_15Pushed, true);
            app.Button_15.BackgroundColor = [0.8 0.8 0.8];
            app.Button_15.Position = [503 239 89 62];
            app.Button_15.Text = '';

            % Create Button_16
            app.Button_16 = uibutton(app.UIFigure, 'push');
            app.Button_16.ButtonPushedFcn = createCallbackFcn(app, @Button_16Pushed, true);
            app.Button_16.BackgroundColor = [0.8 0.8 0.8];
            app.Button_16.Position = [503 61 89 62];
            app.Button_16.Text = '';

            % Create STARTButton
            app.STARTButton = uibutton(app.UIFigure, 'push');
            app.STARTButton.ButtonPushedFcn = createCallbackFcn(app, @STARTButtonPushed, true);
            app.STARTButton.BackgroundColor = [0.3922 0.8314 0.0745];
            app.STARTButton.FontSize = 14;
            app.STARTButton.FontWeight = 'bold';
            app.STARTButton.Position = [114 8 100 25];
            app.STARTButton.Text = 'START';

            % Create GIVEUPButton
            app.GIVEUPButton = uibutton(app.UIFigure, 'push');
            app.GIVEUPButton.ButtonPushedFcn = createCallbackFcn(app, @GIVEUPButtonPushed, true);
            app.GIVEUPButton.BackgroundColor = [0.0745 0.6235 1];
            app.GIVEUPButton.FontSize = 14;
            app.GIVEUPButton.FontWeight = 'bold';
            app.GIVEUPButton.Position = [387 8 100 25];
            app.GIVEUPButton.Text = 'GIVE UP';

            % Create SCOREEditFieldLabel
            app.SCOREEditFieldLabel = uilabel(app.UIFigure);
            app.SCOREEditFieldLabel.HorizontalAlignment = 'right';
            app.SCOREEditFieldLabel.FontSize = 14;
            app.SCOREEditFieldLabel.FontWeight = 'bold';
            app.SCOREEditFieldLabel.FontColor = [1 0 0];
            app.SCOREEditFieldLabel.Position = [17 419 55 22];
            app.SCOREEditFieldLabel.Text = 'SCORE';

            % Create SCOREEditField
            app.SCOREEditField = uieditfield(app.UIFigure, 'numeric');
            app.SCOREEditField.Position = [87 419 100 22];

            % Create TimeLabel
            app.TimeLabel = uilabel(app.UIFigure);
            app.TimeLabel.BackgroundColor = [0.3922 0.8314 0.0745];
            app.TimeLabel.FontSize = 36;
            app.TimeLabel.FontWeight = 'bold';
            app.TimeLabel.FontColor = [1 0 0];
            app.TimeLabel.Position = [387 407 235 52];
            app.TimeLabel.Text = 'Time';

            % Show the figure after all components are created
            app.UIFigure.Visible = 'on';
        end
    end

    % App creation and deletion
    methods (Access = public)

        % Construct app
        function app = memory_puzzle

            % Create UIFigure and components
            createComponents(app)

            % Register the app with App Designer
            registerApp(app, app.UIFigure)

            if nargout == 0
                clear app
            end
        end

        % Code that executes before app deletion
        function delete(app)

            % Delete UIFigure when app is deleted
            delete(app.UIFigure)
        end
    end
end
