# parcial
# pregunta 1
1. Es necesario hacer rezise del vector cuando se llena ya que al hacer la otra opcion de apartar un espacio en memoria
para seguir almacenando los elementos que se van a insertar en el futuro así se deba llevar registro dentro de la clase de que los elementos del vector pueden estar
almacenados en diferentes lugares de la memoria se gastaria mucha mas memoria y seria mas tedioso al manejarlo por eso aunque si se podria es mejor hacer resize.
2. yo creria que para mi las listas enlazadas serian mas efectivas si se realizan muchos resize.

# pregunta 2

1.
- capacidad final:
   vector x= 10240
   
   vector y= 20617
   
   vector z= 12800

- desperdicio en el que incurre los vectores:

   vector x= 240
   
   vector y= 10617
   
   vector z= 2800
   
2. el vector que resulta ser mas eficiente al ejecutar el programa es el vector x ya que el desperdicio de este vector es solo de 240.

# pregunta 3
template <typename L> class list{
private:
  class node{
  private:
    L ciudad;
    node *next;
  public:
    node():ciudad(),next(nullptr) {}
    node(L d):ciudad(d),next(nullptrt) {}
    void setnext (node* n) {next= n};
    void getnext {return next};
    L getciudad () {return ciudad};
  }
private:
  node* first;
  node* last;
  unisgned int size;
  
public:
  list(): first(nullptr), last(nullptr), size(0) {};
  unsigned int getsize const{retunr size;}
  bool empty () const {return first == nullptr;}
  void pushback (L elem) {
    node* n = new node(elem);
    if (empty()){
      first= n;
  } 
  else {
    last->setnext (n);
  }
  last= n;
  size++
  }
  void pushfront(L elem){
    if(empty()){
      pushback(elem);
    } 
    else {
      node* n= new node elem;
      n->setnext(first);
      first= n;
      size++;
    }
  }
}


