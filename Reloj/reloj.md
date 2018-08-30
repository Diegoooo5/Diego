// Codigo
public class Clock {
    public int seg;
    public int min; //atributos
    public int hor;
    
    public Clock(){ 
        this.seg=0;
        this.min=0;
        this.hor=0;
    }
    public Clock(int h,int m,int s){ 
        this.seg=s;
        this.min=m;
        this.hor=h;
    }
    public void sethor(int h){ //hora!
        this.hor=h;
    }
    public int gethor(){
        return(this.hor);
    }
    public void setmin(int m){// minutos!
        this.min=m;
    }
    public int getmin(){
        return(this.min);
    }
    public void setseg(int s){ // segundos!
        this.seg=s;
    }
    public int getseg(){
        return(this.seg);
    }
    public void aumM(){
        if(getmin()+1>59){
        setmin(0);
        sethor(gethor()+1);
        }
       else{
        setmin(getmin()+1);
        }
    }
    
    public void aumentarmin(){
        if (getmin()+1>59){
            //h++ m=0 
            sethor(gethor()+1);
            setmin(0);
    
        }
        else {
            setmin(getmin()+1);
        }
    }
   
      public void sueltaelreloj(){
       System.out.println("Hora->"+gethor()+":"+getmin()+":"+getseg()); 
    
    }
    
    public void Formatoh(){
        if(gethor()<12){
        sueltaelreloj();
        System.out.println("AM");
    
    }
    else {
        sueltaelreloj();
        System.out.println("PM");
    }
    }
    }
