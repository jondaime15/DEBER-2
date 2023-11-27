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

    public void mostrarInformacion() {
        System.out.println("Edificio - Consumo de energía: " + consumoEnergia);
    }
}
