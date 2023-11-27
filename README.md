import java.util.ArrayList;

interface ImpactoEcologico {
    int obtenerImpactoEcologico();
}

class Edificio implements ImpactoEcologico {
    private int consumoEnergia;

    public Edificio(int consumoEnergia) {
        this.consumoEnergia = consumoEnergia;
    }

    @Override
    public int obtenerImpactoEcologico() {
        return consumoEnergia * 5; // Ejemplo simple, ajusta según tus necesidades
    }

    public void mostrarInformacion() {
        System.out.println("Edificio - Consumo de energía: " + consumoEnergia);
    }
}

class Auto implements ImpactoEcologico {
    private int emisionesCO2;

    public Auto(int emisionesCO2) {
        this.emisionesCO2 = emisionesCO2;
    }

    @Override
    public int obtenerImpactoEcologico() {
        return emisionesCO2 * 10; // Ejemplo simple, ajusta según tus necesidades
    }

    public void mostrarInformacion() {
        System.out.println("Auto - Emisiones de CO2: " + emisionesCO2);
    }
}

class Bicicleta implements ImpactoEcologico {
    private boolean esElectrica;

    public Bicicleta(boolean esElectrica) {
        this.esElectrica = esElectrica;
    }

    @Override
    public int obtenerImpactoEcologico() {
        return esElectrica ? 1 : 0; // Ejemplo simple, ajusta según tus necesidades
    }

    public void mostrarInformacion() {
        System.out.println("Bicicleta - Es eléctrica: " + esElectrica);
    }
}

public class Main {
    public static void main(String[] args) {
        Edificio edificio = new Edificio(100);
        Auto auto = new Auto(50);
        Bicicleta bicicleta = new Bicicleta(true);

        ArrayList<ImpactoEcologico> impactoEcologicoArrayList = new ArrayList<>();
        impactoEcologicoArrayList.add(edificio);
        impactoEcologicoArrayList.add(auto);
        impactoEcologicoArrayList.add(bicicleta);

        for (ImpactoEcologico objeto : impactoEcologicoArrayList) {
            int impacto = objeto.obtenerImpactoEcologico();
            System.out.println("Impacto ecológico: " + impacto);

            if (objeto instanceof Edificio) {
                ((Edificio) objeto).mostrarInformacion();
            } else if (objeto instanceof Auto) {
                ((Auto) objeto).mostrarInformacion();
            } else if (objeto instanceof Bicicleta) {
                ((Bicicleta) objeto).mostrarInformacion();
            }
            System.out.println();
        }
    }
}
