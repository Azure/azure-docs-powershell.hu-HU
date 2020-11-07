---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: bfd90797ff60c42927b23424e3c100efd16a6d24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843757"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## Áttekintés
Eltávolítja az alapértelmezett webhelyet egy virtuális hálózati átjáróról.

## SZINTAXISA

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Remove-AzVirtualNetworkGatewayDefaultSite** parancsmag eltávolítja a kényszerített bújtatási alapértelmezett webhelyet egy virtuális hálózati átjáróról.
A kényszeres bújtatás segítségével átirányíthatja az internethez kötött forgalmat az Azure virtuális gépekről a helyszíni hálózatra; Ezzel a beállítással ellenőrizheti és naplózhatja a forgalmat, mielőtt felszabadítja.
A kényszeres bújtatást virtuális magánhálózati (VPN) bújtatási alagúton keresztül valósítják meg; Ehhez az alagúthoz egy alapértelmezett webhelynek kell lennie, egy helyi átjárót, ahol az összes Azure internetes forgalmat átirányítja.

**Eltávolítás – a AzVirtualNetworkGatewayDefaultSite** eltávolítja az átjáróhoz rendelt alapértelmezett webhelyet.
Ha ezt a lehetőséget választja, akkor Set-AzVirtualNetworkGatewayDefaultSite kell használnia egy új alapértelmezett webhely hozzárendelését ahhoz, hogy az átjáró használható legyen a kényszeres bújtatáshoz.

## Példák

### 1. példa: a virtuális hálózati átjáróhoz rendelt alapértelmezett webhely eltávolítása
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

Ez a példa eltávolítja a ContosoVirtualGateway nevű virtuális hálózati átjáróhoz jelenleg hozzárendelt alapértelmezett webhelyet.

Az első parancs a **Get-AzVirtualNetworkGateway** használatával hoz létre objektumot az átjáróhoz; Ez az objektum hivatkozás a $Gateway nevű változóban tárolódik.

A második parancs ezután eltávolítja a **Remove-AzVirtualNetworkGatewayDefaultSite** az átjáróhoz rendelt alapértelmezett webhely eltávolításához.

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

### -VirtualNetworkGateway
Az eltávolítandó alapértelmezett webhelyt tartalmazó virtuális hálózati átjáróhoz tartozó objektum hivatkozását adja meg.
A virtuális hálózati átjáróhoz az Get-AzVirtualNetworkGateway használatával hozhat létre objektum-hivatkozást, és megadhatja az átjáró nevét.

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

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


