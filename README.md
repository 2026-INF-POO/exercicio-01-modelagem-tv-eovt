# Exercício: Modelagem TV

public class TV {
    int tamanho;
    int volume = 5;
    String marca;
    int voltagem;
    int canal = 1;
    boolean ligada = false;

    public TV(int tamanho, String marca, int voltagem) {
        this.tamanho = tamanho;
        this.marca = marca;
        this.voltagem = voltagem;
    }

    public void ligar() {
        ligada = true;
        System.out.println("TV ligada. Consumo: " + (tamanho * voltagem) + "W");
    }

    public void desligar() {
        ligada = false;
        System.out.println("TV desligada.");
    }

    public void aumentarVolume() {
        if(volume < 10) volume++;
        System.out.println("Volume: " + volume);
    }

    public void diminuirVolume() {
        if(volume > 1) volume--;
        System.out.println("Volume: " + volume);
    }

    public void subirCanal() {
        canal++;
        System.out.println("Canal: " + canal);
    }

    public void descerCanal() {
        if(canal > 1) canal--;
        System.out.println("Canal: " + canal);
    }

    public static void main(String[] args) {
        TV minhaTV = new TV(42, "Samsung", 110);
        minhaTV.ligar();
        minhaTV.aumentarVolume();
        minhaTV.subirCanal();
        minhaTV.desligar();
    }
}
