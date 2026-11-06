# Respuestas — Modals, ScrollView y SafeAreaView

## 1. ¿Qué hace la prop `visible` de `Modal` y por qué la controlamos con `useState`?

visible dice si el modal se ve o no. Usamos useState para que, al cambiar el valor, la pantalla se actualice y el modal aparezca o desaparezca.

## 2. ¿Para qué sirve `onRequestClose`? ¿Qué pasa en Android si no cierras el modal ahí?

Se ejecuta cuando el usuario presiona el botón *atrás* de Android. Si ahí no cierras el modal, el botón atrás no hace nada y el modal se queda abierto.

## 3. ¿Qué efecto tiene `transparent={true}`? Nombra los tres valores de `animationType`.

Hace que el fondo del modal sea transparente, así se ve la pantalla de atrás. Los valores de animationType son none, slide y fade.

## 4. ¿Por qué existe `ScrollView`? ¿Qué pasa con un `View` largo sin él? ¿Cuándo usarías `FlatList`?

ScrollView sirve para desplazar contenido que no cabe en la pantalla; un View largo no se desplaza y lo que no cabe se corta. Usaría FlatList para listas muy largas, porque solo dibuja lo que se ve.

## 5. ¿Cuál es la diferencia entre `style` y `contentContainerStyle` en un `ScrollView`?

style es para la caja del ScrollView (tamaño, fondo). contentContainerStyle es para el contenido de adentro (padding, gap, cómo se acomodan los elementos).

## 6. ¿Para qué sirve `SafeAreaView` y qué zonas protege? ¿Por qué usamos `react-native-safe-area-context`?

Sirve para que el contenido no quede debajo del notch ni de las barras de arriba y abajo del teléfono. Usamos react-native-safe-area-context porque funciona en iOS y Android; el de React Native solo funciona en iOS.

## 7. Escribe las tres buenas prácticas del paso 5 con tus palabras y da un ejemplo de cuándo un modal **no** es buena idea.

1. Usar modales solo para cosas cortas, como compartir el perfil.
2. Usar ScrollView para poco contenido y FlatList para listas largas.
3. Poner toda la pantalla dentro de un SafeAreaView.

Un modal no es buena idea para un formulario largo; para eso es mejor una pantalla nueva.
