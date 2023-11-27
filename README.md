public class Edificio implements ImpactoEcologico {
    private int consumoEnergia;

    public Edificio(int consumoEnergia) {
        this.consumoEnergia = consumoEnergia;
    }

    @Override
    public int obtenerImpactoEcologico() {
        // Lógica para calcular el impacto ecológico del edificio
        return consumoEnergia * 5; // Ejemplo simple, ajusta según tus necesidades
    }

    public void mostrarInformacion() {
        System.out.println("Edificio - Consumo de energía: " + consumoEnergia);
 public class Edificio implements ImpactoEcologico {
    private int consumoEnergia;

    public Edificio(int consumoEnergia) {
        this.consumoEnergia = consumoEnergia;
    }

    @Override
    public int obtenerImpactoEcologico() {
        // Lógica para calcular el impacto ecológico del edificio
        return consumoEnergia * 5; // Ejemplo simple, ajusta según tus necesidades
    }

public Bicicleta(boolean esElectrica) {
        this.esElectrica = esElectrica;
    }

    @Override
    public int obtenerImpactoEcologico() {
        // Lógica para calcular el impacto ecológico de la bicicleta
        return esElectrica ? 1 : 0; // Ejemplo simple, ajusta según tus necesidades
    }

    public void mostrarInformacion() {
        System.out.println("Bicicleta - Es eléctrica: " + esElectrica);
    }
}
