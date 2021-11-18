- 👋 Hi, I’m @ByeDarkHope
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- ###  RPG: Folha de Personagem

- Uma página de ficha de personagem para RPG inspirada / copiada da ** [ Ordem Paranormal: Desconjuração ] (https://www.youtube.com/watch?v=b7PvLWZR6pg "Ordem Paranormal: Desconjuração") ** , fiz com intuito de estudar e praticar HTML e CSS;
- Uma página de ficha de personagem para RPG inspirada / copiada de ** [ Ordem Paranormal: Julgamento Errado ] (https://www.youtube.com/watch?v=b7PvLWZR6pg "Ordem Paranormal: Julgamento Errado") ** , eu fiz para estudar e praticar HTML e CSS;

---

<!---
ByeDarkHope/ByeDarkHope is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
$ ( documento ) . pronto ( função ( ) {

     dados  const =  {
        nome : "Claudio" ,
        jogador : "Ryan" ,
        ocupação : "Caçador" ,
        idade : 21 ,
        sexo : "masculino" ,
        local de nascimento : "São paulo" ,
        residência : "São paulo" ,

        vida : {
            atual : 11 ,
            máx : 11 ,
        } ,
        sanidade : {
            atual : 32 ,
            máx : 40 ,
        } ,

        armas : [
            {
                nome : "Balestra" ,
                tipo : "Arco" ,
                damege : "1d20" ,
                numCurrent : 1 ,
                numMax : 1 ,
                ataque : 5 ,
                alcance : "10 m" ,
                defeito : 1 ,
                área : "" ,
            } ,
            {
                nome : "Canivite" ,
                tipo : "Briga" ,
                damege : "1d10" ,
                numCurrent : "" ,
                numMax : "" ,
                ataque : "1/2" ,
                alcance : "" ,
                defeito : 1 ,
                área : "" ,
            } ,
        ] ,
    }

    dados . armas . mapa ( ( arma ,  índice )  =>  {
        addWeaponToTable ( arma ,  índice ) ;
    } ) ;


    $ ( "#nome" ) . val ( dados . nome ) ;
    $ ( "#player" ) . val ( dados . jogador ) ;
    $ ( "#occupation" ) . val ( dados . ocupação ) ;
    $ ( "#age" ) . val ( dados . idade ) ;
    $ ( "#sex" ) . val ( dados . sexo ) ;
    $ ( "#birthplace" ) . val ( dados . local de nascimento ) ;
    $ ( "#residence" ) . val ( dados . residência ) ;

    $ ( ".lifeBar" ) . css ( "largura" ,  ` $ { calculBar ( dados . vida . corrente ,  dados . vida . max ) } %` ) ;
    $ ( ".sanityBar" ) . css ( "largura" ,  ` $ { calculBar ( dados . sanidade . atual ,  dados . sanidade . max ) } %` ) ;


    const  diceModal  =  $ ( "#diceAttributes" ) ;
    const  lifeModal  =  $ ( "#lifeModal" ) ;
    const  sanityModal  =  $ ( "#sanityModal" ) ;

    $ ( janela ) . clique ( função ( evento )  {
        if  ( event . target . id  ==  "diceAttributes" )  {
            diceModal . css ( "display" ,  "none" ) ;
            $ ( "#diceNumber" ) . texto ( "" ) ;
            $ ( "#diceType" ) . texto ( "" ) ;

            $ ( ".modalDice" ) . css ( "transformar" ,  "girar (0deg)" ) ;
            $ ( ".modalDice" ) . css ( "-webkit-transform" ,  "rotate (0deg)" ) ;
        } else  if  ( event . target . id  ==  "lifeModal" )  {
            lifeModal . css ( "display" ,  "none" ) ;
        } else  if  ( event . target . id  ==  "sanityModal" )  {
            sanityModal . css ( "display" ,  "none" ) ;
        } else  if  ( event . target . id  ==  "addWeaponModal" )  {
            closeModal ( "#addWeaponModal" ) ;
        }
    } ) ;

    $ ( "#btn" ) . click ( function ( ) {

        console . log ( este )

        diceModal . css ( "exibir" ,  "bloquear" ) ;

        setTimeout ( ( )  =>  {
            $ ( ".modalDice" ) . css ( "transformar" ,  "girar (360deg)" ) ;
            $ ( ".modalDice" ) . css ( "-webkit-transform" ,  "rotate (360deg)" ) ;
        } ,  1000 ) ;

        setTimeout ( ( )  =>  {

            var  diceNumber  =  Math . chão ( matemática . aleatório ( )  *  21 ) ;
            $ ( "#diceNumber" ) . texto ( diceNumber ) ;
            $ ( "#diceType" ) . texto ( "BOM" ) ;

            setTimeout ( ( )  =>  {
                diceModal . css ( "display" ,  "none" ) ;
                $ ( "#diceNumber" ) . texto ( "" ) ;
                $ ( "#diceType" ) . texto ( "" ) ;

                $ ( ".modalDice" ) . css ( "transformar" ,  "girar (0deg)" ) ;
                $ ( ".modalDice" ) . css ( "-webkit-transform" ,  "rotate (0deg)" ) ;
            } ,  20.000 ) ;
        } ,  2000 ) ;
    } ) ;

    $ ( ".lifeBar" ) . click ( function ( ) {

        console . log ( isto ) ;
        lifeModal . css ( "exibir" ,  "bloquear" ) ;
    } ) ;

    $ ( ".sanityBar" ) . click ( function ( ) {

        console . log ( isto ) ;
        sanityModal . css ( "exibir" ,  "bloquear" ) ;
    } ) ;

    $ ( "#addWeapon" ) . click ( function ( ) {
        openModal ( "#addWeaponModal" ) ;
    } ) ;

    $ ( '#lesion' ) . alterar ( função ( )  {
        se ( isto . verificado )  {
            console . log ( 'Modo lesionamendo grave ativado!' ) ;
        } else  {
            console . log ( 'Modo lesionamendo grave desativado!' ) ;
        } 
    } ) ;

    $ ( '#injury' ) . alterar ( função ( )  {
        se ( isto . verificado )  {
            console . log ( 'Modo lesionamendo ativado!' ) ;
        } else  {
            console . log ( 'Modo lesionado desativado!' ) ;
        } 
    } ) ;

    $ ( '#dying' ) . alterar ( função ( )  {
        se ( isto . verificado )  {
            console . log ( 'Modo morrendo ativado!' ) ;
        } else  {
            console . log ( 'Modo morrendo desativado!' ) ;
        } 
    } ) ;

    $ ( '#traumatized' ) . alterar ( função ( )  {
        se ( isto . verificado )  {
            console . log ( 'Modo traumatizado ativado!' ) ;
        } else  {
            console . log ( 'Modo traumatizado desativado!' ) ;
        } 
    } ) ;

    $ ( '#crazed' ) . alterar ( função ( )  {
        se ( isto . verificado )  {
            console . log ( 'Modo enlouquecido ativado!' ) ;
        } else  {
            console . log ( 'Modo enlouquecido desativado!' ) ;
        } 
    } ) ;

    $ ( '#addWeaponForm' ) . enviar ( função (  evento  )  {

        var  weaponType  =  "" ;

        if ( $ ( "#weaponType" ) . val ( )  ==  "fogo" ) {
            weaponType  =  "Fogo" ;
        } else  if ( $ ( "#weaponType" ) . val ( )  ==  "arch" )  {
            weaponType  =  "Arco" ;
        } else  if ( $ ( "#weaponType" ) . val ( )  ==  "lutar" )  {
            weaponType  =  "Briga" ;
        }

         arma  const =  {
            nome : $ ( "#weaponName" ) . val ( ) ,
            tipo : weaponType ,
            damege : $ ( "#weaponDamege" ) . val ( ) ,
            numCurrent : $ ( "#weaponNumCurrent" ) . val ( ) ,
            numMax : $ ( "#weaponNumMax" ) . val ( ) ,
            ataque : $ ( "#weaponAttack" ) . val ( ) ,
            alcance : $ ( "#weaponReach" ) . val ( ) ,
            defeito : $ ( "#weaponDefect" ) . val ( ) ,
            área : $ ( "#weaponArea" ) . val ( ) ,
        }

        dados . armas . empurrar ( arma ) ;
        const  id  =  data . armas . comprimento - 1 ;
        addWeaponToTable ( arma ,  id ) ;

        closeModal ( "#addWeaponModal" ) ;
        evento . preventDefault ( ) ;
    } ) ;
} ) ;

função  calculaBar ( corrente ,  máx. ) {
    if  ( atual  >  max ) {
        return  100 ;
    }  else  if  ( atual  <  0 )  {
        return  0 ;
    }  else  {
         valor  const =  ( 100 / máx. ) * atual ;
         string  const =  value . toString ( ) . dividir ( "." ) [ 0 ] ;
         porcentagem  const =  Número ( string ) ;
         porcentagem de retorno ;
    }
}

function  openModal ( modal ) {
    const  Modal  =  $ ( modal ) ;
    Modal . css ( "exibir" ,  "bloquear" ) ;
}

function  closeModal ( modal ) {
    const  Modal  =  $ ( modal ) ;
    Modal . css ( "display" ,  "none" ) ;
}

function  addWeaponToTable ( weapon ,  id )  {
    const  newWeapon  =  $ ( `<tr id =" $ { id } ">
        <td>
            <button onclick = "deleteWeapon ( $ { id } )">
                <i class = "fa fa-trash-o trashcan"> </i>
            </button>
            $ { arma . nome }
        </td>
        <td> $ { arma . type } </td>
        <td> $ { arma . damege } </td>
        <td> $ { arma . numCurrent } </td>
        <td> $ { arma . numMax } </td>
        <td> $ { arma . ataque } </td>
        <td> $ { arma . alcance } </td>
        <td> $ { arma . defeito } </td>
        <td> $ { arma . área } </td>
    </tr> ` ) ;
    $ ( "mesa # armas" ) . append ( newWeapon ) ;
}

function  deleteWeapon ( id )  {
    $ ( `tr # $ { id } ` ) . remove ( ) ;
} 
 BIN +21 KB img / character.png 
Arquivo binário não mostrado.
 BIN +5,76 KB img / dado.png 
Arquivo binário não mostrado.
 7  img / trashcan.svg 
@@ -0,0 +1,7 @@
<? xml  version = " 1.0 "  encoding = " utf-8 " ?>
<! - Svg Vector Icons: http://www.onlinewebfonts.com/icon ->
<! DOCTYPE  svg PUBLIC "- // W3C // DTD SVG 1.1 // EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
< svg  version = " 1.1 "  xmlns = " http://www.w3.org/2000/svg "  xmlns : xlink = " http://www.w3.org/1999/xlink "  x = " 0px "  y = " 0px "  viewBox = " 0 0 1000 1000 "  enable-background = " new 0 0 1000 1000 "  xml : space = " preserve " >
< metadados > Ícones de vetor Svg: http://www.onlinewebfonts.com/icon </ metadata >
<g> <g transform = "translate (0.000000.511.000000) scale (0.100000, -0.100000)"> <path d = "M3471.7,4965.7c-51.3-23.3-121.3-72.3-156.3-109.7c-116.7- 126-135.3-207.7-135.3-616v-373.3H2060c-1057,0-1127-2.3-1208.7-44.3C751,3771.681,3698.7,627.3,3593.7C597,3533,590,3435,590,3040.7c0-466,7, 0-478.3,51.3-513.3c42-30.3,128.3-37.3.443.3-37.3h392V-956.3c0-3306.3,2.3-3453.3,44.3-3542c53.7-114.3,149.3-207.7.263.7-254.3c77-32.7.438.7- 37.3,3220-37.3c3000.7,0,3138.3,2.3,3227,44.3C8346-4692,8439.3-4596.3,8486-4482c32.7,77,37.3,471.3,37.3,3530.3V2490h392c315,0,401.3,7,443.3,37.3c51. 3,35,51,3,46,7,51,3,513,3c0,518-14,583,3-144,7,700c-140,128,3-114,3,126-1323,126h-1120l-7,406l-7,406l-72,3,91c-88,7,107,3-198,3,184,3 -310.4,217c-51.3,14-613.7,23.3-1472.3,23.3C3651.3,5010,3560.3,5005.3,3471.7,4965.7z M6423.3,4725.3c58.3-30.3,119-79.3,133-112c18.7 -37.3,30.3-177.3,30.3-401.3v-345.3H5000H3413.3v347.7c0,191.3,9.3.375.7,23.3.408.3c11.7,32.7.56,81.7,98,107.3c74.7,44.3,119,46.7,1430.3, 46.7h1355.7L6423.3,4725.3z M9057.7,3600.7c102.7-53.7,119-123.7,119-504v-350H5000H823.3v368.7c0,389.7,11.7,427,128.3,490c32.7,18.7,1183,25.7, 4043.7,28C8409,3633.3,9001.7,3628.7,9057.7,3600.7z M8290-928.3c0-3791.7,11.7-3525.7-151.7-3595.7c-119-49-6157.7-49-6276.7,0c-163.3,70-151.7-196- 151.7,3595.7V2490h3290h3290V-928.3z "/> <path d =" M3217.3,1636c-32.7-32.7-37.3-305.7-37.3-2667c0-2013.7,7-2636.7,28-2657.7c35-35,142.3-35,177.3,0c21, 21,28.644,28,2657.7c0,2361.3-4.7,2634.3-37.3,2667c-18.7,21-56,37.3-79.3,37.3S3236,1657,3217.3,1636z "/> <caminho d =" M4920.7,1636c -32.7-32.7-37.3-305.7-37.3-2667c0-2013.7,7-2636.7,28-2657.7c35-35,142,3-35,177,3,0c21,21,28,644,28,2657,7c0,2361,3-4,7,2634,3-37,3,2667c-18,7 ,21-56,37.3-79.3,37.3C4976.7,1673.3,4939.3,1657,4920.7,1636z "/> <path d =" M6624,1636c-32.7-32.7-37.3-305.7-37.3-2667c0-2013.7,7- 2636.7,28-2657.7c44.3-44.3,154-35,182,16.3c16.3,30.3,23.3.903,23.3,2660c0,2342.7-4.7,2615.7-37.3,2648.3c-18.7,21-56,37.3-79.3 , 37.3C6680,1673.3,6642,7,1657,6624,1636z "/> </g> </g>
</ svg > 
 292  index.html 
@@ -0,0 +1.292 @@
<! DOCTYPE html >
< html  lang = " pt-br " >
    < cabeça >
        < meta  charset = " UTF-8 " >
        < meta  name = " viewport " content = " width = device-width, initial-scale = 1.0 " >
        < script  src = " https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js " > </ script >
        < link  rel = " stylesheet " href = " https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css " >

        < link  rel = " stylesheet " href = " styles.css " >
        < script  src = " characterSheet.js " > </ script >

        < title > Ficha do personagem </ title >
    </ head >
    < corpo >
        < h1  class = " title " > Perfil de investigador </ h1 >

        <! - Acionar / abrir o modal ->

        <! - O modal ->
        < div  id = " diceAttributes " class = " modal " >

            <! - Conteúdo modal ->
            < div  class = " modal-content " >
                < img  class = " modalDice " src = " ./img/dado.png " alt = " Dado " >
                < h2  id = " diceNumber " > </ h2 >
                < p  id = " diceType " > </ p >
            </ div >

        </ div >

        < div  id = " lifeModal " class = " modal with-input " >
            < div  class = " modal-content " >
                < h2 > VIDA MODIFICAR </ h2 >
                < hr >
                < form  action = "" >
                    < h3 > Atual </ h3 >
                    < input  type = " text " name = " lifeCurrent " id = " lifeCurrent " >
                    < h3 > Máximo </ h3 >
                    < Entrada  tipo = " texto " nome =" Lifemax " id =" Lifemax " > < br >
                    < input  type = " submit " value = " Salvar " >
                </ form >
            </ div >
        </ div >

        < div  id = " sanityModal " class = " modal with-input " >
            < div  class = " modal-content " >
                < h2 > SANIDADE MODIFICAR </ h2 >
                < hr >
                < form  action = "" >
                    < h3 > Atual </ h3 >
                    < input  type = " text " name = " sanityCurrent " id = " sanityCurrent " >
                    < h3 > Máximo </ h3 >
                    < Entrada  tipo = " texto " nome =" sanityMax " id =" sanityMax " > < br >
                    < input  type = " submit " value = " Salvar " >
                </ form >
            </ div >
        </ div >

        < div  id = " addWeaponModal " class = " modal with-input " >
            < div  class = " modal-content " >
                < h2 > ARMA ADICIONAR </ h2 >
                < hr >
                < form  id = " addWeaponForm " action = "" >
                    < table  class = " armas " id = " newWeapon " >
                        < tr >
                            < th > Nome </ th >
                            < th > Tipo </ th >
                            < th > Dano </ th >
                            < th > Num. Atual </ th >
                            < th > Num. Máximo </ th >
                            < th > Ataque </ th >
                            < th > Alcance </ th >
                            < th > Defeito </ th >
                            < th > Área </ th >
                        </ tr >
                        < tr >
                            < td >
                                < input  type = " text " name = " weaponName " id = " weaponName " >
                            </ td >
                            < td >
                                < select  id = " weaponType " name = " weaponType " >
                                    < option  value = " fire " > Fogo </ option >
                                    < option  value = " arch " > Arco </ option >
                                    < option  value = " fight " > Briga </ option >
                                </ select >
                            </ td >
                            < td >
                                < input  type = " text " name = " weaponDamege " id = " weaponDamege " >
                            </ td >
                            < td >
                                < input  type = " text " name = " weaponNumCurrent " id = " weaponNumCurrent " >
                            </ td >
                            < td >
                                < input  type = " text " name = " weaponNumMax " id = " weaponNumMax " >
                            </ td >
                            < td >
                                < input  type = " text " name = " weaponAttack " id = " weaponAttack " >
                            </ td >
                            < td >
                                < input  type = " text " name = " weaponReach " id = " weaponReach " >
                            </ td >
                            < td >
                                < input  type = " text " name = " weaponDefect " id = " weaponDefect " >
                            </ td >
                            < td >
                                < input  type = " text " name = " weaponArea " id = " weaponArea " >
                            </ td >
                        </ tr >
                    </ mesa >
                    < input  type = " submit " value = " Salvar " >
                </ form >
            </ div >
        </ div >

        < div  class = " container " >
            < div  class = " details border " >
                < h2  class = " grid-title " > DETALHES PESSOAIS </ h2 >
                < hr >

                < div  class = " inputs " >
                    < h4 > Nome </ h4 >
                    < input  type = " text " name = " name " id = " name " value = "" >
                    < h4 > Jogador </ h4 >
                    < input  type = " text " name = " player " id = " player " value = "" >
                    < h4 > Ocupação </ h4 >
                    < input  type = " text " name = " profissão " id = " profissão " value = "" >
                    < h4 > Idade </ h4 >
                    < input  type = " text " name = " age " id = " age " value = "" >
                    < h4 > Sexo </ h4 >
                    < selecione  id = " sexo " name = " sexo " >
                        < option  value = " male " > Masculino </ option >
                        < option  value = " female " > Feminino </ option >
                        < option  value = " other " > Outros </ option >
                    </ select >
                    < h4 > Local de nascimento </ h4 >
                    < input  type = " text " name = " birthplace " id = " birthplace " value = "" >
                    < h4 > Local de residência </ h4 >
                    < input  type = " text " name = " residence " id = " residence " value = "" >
                </ div >
            </ div >
            < div  class = " personagem " >
                < div  class = " characterHeader " >
                    < img  class = " characterPhoto " src = " ./img/character.png " alt = " Foto " >
                    < img  class = " dice " src = " ./img/dado.png " alt = " Dado " >
                </ div >

                < div  class = " bars " >
                    < h4 > Vida </ h4 >
                    < div  class = " bar " >
                        < div  class = " lifeBar " > </ div >
                    </ div >
                    < div  class = " checkboxs " >
                        < form  action = "" >
                            < input  type = " checkbox " id = " lesion " name = " lesion " value = " lesion " >
                            < label  for = " lesion " > Lesão grave </ label >
                            < input  type = " checkbox " id = " lesão " name = " lesão " value = " lesão " >
                            < Rótulo  para = " lesão " > Lesionamento </ rótulo >
                            < input  type = " checkbox " id = " morrendo " name = " morrendo " value = " morrendo " >
                            < label  for = " dying " > Morrendo </ label >
                        </ form >
                    </ div >

                    < h4 > Sanidade </ h4 >
                    < div  class = " sanity " >

                        < div  class = " contentSanityBar " >
                            < div  class = " sanityBar " > </ div >
                        </ div >
                        < img  class = " sanityDice " src = " ./img/dado.png " alt = " Dado " >
                    </ div >
                    < div  class = " checkboxs " >
                        < input  type = " checkbox " id = " traumatized " name = " traumatized " value = " traumatized " >
                        < label  for = " traumatized " > Traumatizado </ label >
                        < input  type = " checkbox " id = " crazed " name = " crazed " value = " crazed " >
                        < label  for = " crazed " > Enlouquecido </ label >
                    </ div >
                </ div >

                < div  class = " extra " >
                    < div  class = " damage " >
                        < h3 > Dano extra </ h3 >
                        < input  type = " text " name = " dano " id = " dano " >
                    </ div >
                    < div  class = " body " >
                        < h3 > Corpo </ h3 >
                        < input  type = " text " name = " dano " id = " dano " >
                    </ div >
                    < div  class = " exposição " >
                        < H3 > Exposição < br > paranormal </ h3 >
                        < input  type = " text " name = " dano " id = " dano " >
                    </ div >
                </ div >
            </ div >
            < div  class = " attribute border " >
                < h2  class = " grid-title " > ATRIBUTOS </ h2 >
                < hr >

                < div  class = " attributeList " >
                    < div  class = " attribute " >
                        < A  id = " btn " >
                            < img  class = " attributeDice " src = " ./img/dado.png " alt = " Dado " >
                        </ a >
                        < h3 > Aparência </ h3 >
                        < input  type = " text " name = " attribute " id = " attribute " >
                    </ div >
                    < div  class = " attribute " >
                        < A  onclick = " alert (1); " >
                            < img  class = " attributeDice " src = " ./img/dado.png " alt = " Dado " >
                        </ a >
                        < h3 > Constituição </ h3 >
                        < input  type = " text " name = " attribute " id = " attribute " >
                    </ div >
                    < div  class = " attribute " >
                        < A  onclick = " alert (1); " >
                            < img  class = " attributeDice " src = " ./img/dado.png " alt = " Dado " >
                        </ a >
                        < h3 > Destreza </ h3 >
                        < input  type = " text " name = " attribute " id = " attribute " >
                    </ div >
                    < div  class = " attribute " >
                        < A  onclick = " alert (1); " >
                            < img  class = " attributeDice " src = " ./img/dado.png " alt = " Dado " >
                        </ a >
                        < h3 > Educação </ h3 >
                        < input  type = " text " name = " attribute " id = " attribute " >
                    </ div >
                    < div  class = " attribute " >
                        < A  onclick = " alert (1); " >
                            < img  class = " attributeDice " src = " ./img/dado.png " alt = " Dado " >
                        </ a >
                        < h3 > Força </ h3 >
                        < input  type = " text " name = " attribute " id = " attribute " >
                    </ div >
                    < div  class = " attribute " >
                        < A  onclick = " alert (1); " >
                            < img  class = " attributeDice " src = " ./img/dado.png " alt = " Dado " >
                        </ a >
                        < h3 > Inteligência </ h3 >
                        < input  type = " text " name = " attribute " id = " attribute " >
                    </ div >
                    < div  class = " attribute " >
                        < A  onclick = " alert (1); " >
                            < img  class = " attributeDice " src = " ./img/dado.png " alt = " Dado " >
                        </ a >
                        < h3 > Poder </ h3 >
                        < input  type = " text " name = " attribute " id = " attribute " >
                    </ div >
                    < div  class = " attribute " >
                        < A  onclick = " alert (1); " >
                            < img  class = " attributeDice " src = " ./img/dado.png " alt = " Dado " >
                        </ a >
                        < h3 > Sorte </ h3 >
                        < input  type = " text " name = " attribute " id = " attribute " >
                    </ div >
                </ div >

            </ div >
            < div  class = " expertise border " >
                < h2  class = " grid-title " > PERICIA </ h2 >
                < hr >
            </ div >
            < div  class = " combat border " >
                < div  class = " combatHeader " >
                    < h2  class = " grid-title " > COMBATE </ h2 >
                    < button  id = " addWeapon " > & plus; </ botão >
                </ div >
                < hr >

                < tabela de  classes = " armas " id = " armas " >
                    < tr >
                        < th > Nome </ th >
                        < th > Tipo </ th >
                        < th > Dano </ th >
                        < th > Freira. Atual </ th >
                        < th > Num. Máximo </ th >
                        < th > Ataque </ th >
                        < th > Alcance </ th >
                        < th > Defeito </ th >
                        < th > Área </ th >
                    </ tr >

                </ mesa >

            </ div >

            < div  class = " expertise2 border " >
                < h2  class = " grid-title " > PERICIA </ h2 >
                < hr >
            </ div >
        </ div >
    </ body >
</ html > 
