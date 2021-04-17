class Staff{
  private int hWorked = 10;
  public int hNextWorked = 11;
  private int partsOfWork = 1;

  public int HoursWorked
  {
    get
    {
      return hWorked;
    }
    set
    {
      if (value > 0){
        hWorked = value;
      }
      else{
        hWorked = 0;
      }
    }
  }

  public int PartsWorked
  {
    get
    {
      return partsOfWork;
    }
    set
    {
      if (value > 1){
        partsOfWork = value;
      }
      else{
        partsOfWork = 1;
      }
    }
  }

  public double HoursInPart()
  {
    return hWorked /(double) partsOfWork;
  }
}

Staff staff = new Staff();

staff.HoursWorked = 10;
staff.PartsWorked = 2;
double hInPart = staff.HoursInPart();
