import com.mycompany.calculadora2.Calculadora2;
import org.junit.jupiter.api.AfterEach;
import org.junit.jupiter.api.AfterAll;
import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.BeforeAll;
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;
import org.junit.jupiter.params.ParameterizedTest;
import org.junit.jupiter.params.provider.CsvSource;

public class Calculadora2 {

    public Calculadora2() {
    }

    @BeforeAll
    public static void setUpClass() {
        // Inicialización de recursos necesarios para todas las pruebas.
    }

    @AfterAll
    public static void tearDownClass() {
        // Limpieza de recursos utilizados en todas las pruebas.
    }

    @BeforeEach
    public void setUp() {
        // Configuración antes de cada prueba.
    }

    @AfterEach
    public void tearDown() {
        // Limpieza después de cada prueba.
    }


    @Test
    public void testSuma() {
        int resultado1 = Calculadora2.suma(10, 5);
        assertEquals(15, resultado1);
        assertNotEquals(2, resultado1);
    }


    @Test
    public void testResta() {
        int resultado1 = Calculadora2.resta(10, 5);
        assertEquals(5, resultado1);
        assertNotEquals(2, resultado1);
    }


    @ParameterizedTest
    @CsvSource({
        "1, 2, 3",
        "2, 3, 5",
        "-1, -2, -3",
        "0, 0, 0",
        "100, 200, 300"
    })
    public void testSumaParametrizada(int a, int b, int resultadoEsperado) {
        assertEquals(resultadoEsperado, Calculadora2.suma(5, 10));
    }
}
