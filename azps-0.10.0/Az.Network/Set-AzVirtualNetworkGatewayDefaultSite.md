---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 560053ca6b5e49ffcef8dbb6ee4b0ba32f3ed276
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843566"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## Áttekintés
A virtuális hálózati átjáró alapértelmezett webhelyének beállítása.

## SZINTAXISA

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzVirtualNetworkGatewayDefaultSite** parancsmag kényszerített bújtatási alapértelmezett webhelyet rendel egy virtuális hálózati átjáróhoz.
A kényszeres bújtatás segítségével átirányíthatja az internethez kötött forgalmat az Azure virtuális gépekről a helyszíni hálózatra; Ezzel a beállítással ellenőrizheti és naplózhatja a forgalmat, mielőtt felszabadítja.
A kényszeres bújtatást virtuális magánhálózati (VPN) bújtatási alagúton keresztül valósítják meg; Ehhez az alagúthoz egy alapértelmezett webhelynek kell lennie, egy helyi átjárót, ahol az összes Azure internetes forgalmat átirányítja.
A **set-AzVirtualNetworkGatewayDefaultSite** lehetővé teszi az átjáróhoz rendelt alapértelmezett webhely módosítását.

## Példák

### Példa 1: alapértelmezett webhely hozzárendelése virtuális hálózati átjáróhoz
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

Ez a példa egy alapértelmezett webhelyet rendel el egy ContosoVirtualGateway nevű virtuális hálózati átjáróhoz.

Az első parancs egy ContosoLocalGateway nevű helyi átjáróhoz hoz létre egy objektumot.
A $LocalGateway nevű változóban tárolt objektum hivatkozása az alapértelmezett webhelyként konfigurálni kívánt átjárót jelenti.

.
A második parancs Ezután létrehoz egy objektumot a virtuális hálózati átjárónak, és az eredményt az $VirtualGateway nevű változóban tárolja.

A harmadik parancs a **set-AzVirtualNetworkGatewayDefaultSite** parancsmagot használva rendeli hozzá az alapértelmezett webhelyet a ContosoVirtualGateway-hoz.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewayDefaultSite
A megadott virtuális hálózat alapértelmezett webhelyének adja meg a helyi hálózati átjáróhoz tartozó objektum hivatkozását.
A Get-AzLocalNetworkGateway parancsmaggal egy helyi átjáróra mutató objektumra mutató hivatkozást is létrehozhat.

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Annak a virtuális hálózati átjárónak az objektum hivatkozását adja meg, amelybe az alapértelmezett webhelyet hozzá szeretné rendelni.
Létrehozhat egy objektumot a virtuális hálózati átjáróhoz a **Get-AzVirtualNetworkGateway** , és megadhatja az átjáró nevét.

A változó $VirtualGateway ezután a *VirtualNetworkGateway* paraméter paraméterének értékeként használhatók:

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

###  
Ez a parancsmag a **Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway** objektum pipeline-példányait fogadja el.

## KIMENETEK

###  
Ez a parancsmag módosítja a **Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway** objektum meglévő példányait.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


