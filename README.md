<h1>Convention de nommage PHP</h1>

<h2>Nommage</h2>

class MaClasseConcrete extends BaseMaClasseAbstraite implements InterfaceMonInterface {

 const UNE_CONSTANTE = "une valeur";

    public $proprietePublique;

    protected $_proprieteProtegee;

    private $_proprietePrivee;

    public function __construct () {
        // ...
    }

    public static function getFoo () {
        return "foo";
    }

    protected function _setBar ($b) {
        $this->_bar = $b;
    }
}

<h2>Commentaires</h2>

/**
 * Classe Foo qui ne sert visiblement pas à grand-chose
 *
 * Description longue (et inutile)
 * de ma classe qui peut s'étaler
 * sur plusieurs lignes.
 *
 * @package libs
 * @subpackage util
 * @author Benjamin DELESPIERRE <benjamin.delespierre@gmail.com>
 * @version 1.0.0
 * @since 1.2
 * @copyright 2013 Foo Corp.
 */
class Foo extends Bar implements Baz {

    /**
     * Nom
     * @var string
     */
    protected $_name;

    /**
     * Constructeur
     *
     * Description longue (et inutile)
     * de mon constructeur qui peut
     * s'étaler sur plusieurs lignes
     *
     * @param string $name Le nom
     *
     * @throws InvalidArgumentException Si $name n'est pas une chaine
     */
    public function __construct ($name) {
        $this->_name = $name;
    }

    /**
     * toString
     *
     * @return string
     */
    public function __toString () {
        return "Je m'appelle $this->_name";
    }
}
