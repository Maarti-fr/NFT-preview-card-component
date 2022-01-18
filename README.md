Challenge Termier en 2h30.

C'était mon premier challengeLes difficultés:
1 - centrer la carte aux milieux 
2 - le padding a l'intérieur de la carte 
3 - Animation sur l'image du NFTLes solutions de la difficulté;

1 - code :
        position: absolute;
        margin: auto;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;

position: absolute (me permet de placer ma carte grace à top, right, bottom, left car il est détaché des autres blocs et il est positionné par rapport à son ancêtre le plus proche en l'occurrence du body dans ce cas) 
margin: auto (me permettent de placer une marge identique sur les 4 côtés en fonction de la taille de la page)

2 - code :
        box-sizing: border-box 
        
(il delite la taille de la carte et rajoute donc le padding vers l'interieur)

3 - code :

        (je crée un filtre à cote de l'image et là mais en opacité 0 en temps normal)

        .filtre {
            transition: .5s ease;
            opacity: 0;
            position: absolute;
            top: 30%;
            left: 50%;
            transform: translate(-50%, -50%);
            -ms-transform: translate(-50%, -50%);
        }

        (Quand mon curseur et sur l'image je diminue l'opacité)

        .img_NFT:hover .img_main {
            opacity: 0.3;
        }

        (Quand mon curseur et sur l'image j'augmente l'opacité)

        .img_NFT:hover .filtre {
            opacity: 1;
        }

        (je crée l'image qui vient sur l'image NFT)

        .icon_view {
            background-color: hsla(178, 100%, 50%, .4);
            display: block;
            max-width: 260px;
            height: auto;
            border-radius: 15px;
            padding: 106px;
        }



À améliorer :
- Meilleure gestion des flex
- Meilleure compréhension de : hover pour les images
- Rapidité du code