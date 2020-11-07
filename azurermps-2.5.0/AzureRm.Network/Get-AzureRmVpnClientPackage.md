---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientpackage
schema: 2.0.0
ms.openlocfilehash: 193353a3e578ec0f644be605498214d5bf4944c6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849174"
---
# Get-AzureRmVpnClientPackage

## Áttekintés
Információt kap a VPN-ügyfél csomagról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmVpnClientPackage** parancsmag információt kap a virtuális hálózati átjáróból elérhető VPN-ügyfél-csomagokról.
Az ügyfél csomagjai olyan konfigurációs adatokat tartalmaznak, amelyek lehetővé teszik, hogy egy ügyfélszámítógép virtuális MAGÁNHÁLÓZATI kapcsolatot hozzon létre egy Azure virtuális hálózattal; a VPN-kapcsolat létrehozásához az ügyfélgépeknek telepítve kell lenniük a megfelelő konfigurációs csomagnak.
Az ügyfélszámítógép Windows-verziójának (például a Windows 7 vagy a Windows 10) és az ügyfélszámítógép processzor-architektúrájának (AMD64 vagy x86) alapján is elérhetők a különféle konfigurációs csomagok.
A **Get-AzureRmVpnClientPackage** futtatásakor meg kell adnia az architektúra típusát.

## Példák

### 1. példa: adatok beszerzése a processzor-architektúra VPN-csomagról
```
PS C:\>Get-AzureRmVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

Ez a parancs információt kap a ContosoVirtualNetworkGateway nevű virtuális hálózati átjáróban tárolt AMD64 VPN-csomagokról.
Ha információkat szeretne kapni az x86-os ügyfél-csomagokról, állítsa az *ProcessorArchitecture* paraméter értékét x86 értékre.

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

### -ProcessorArchitecture
Annak a CPU-architektúrának a típusát adja meg, amelyre az ügyfél-csomag van tervezve.
Az érvényes értékek az Amd64 és az x86.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.

Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Annak a virtuális hálózati átjárónak a neve, amelybe az ügyfél-csomag adatai vannak tárolva.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Karakterlánc
A ' ResourceGroupName ' paraméter a "string" típusú értéket fogadja el a csővezetékről

### Karakterlánc
A ' VirtualNetworkGatewayName ' paraméter a "string" típusú értéket fogadja el a csővezetékről

## KIMENETEK

###  
A **Get-AzureRmVpnClientPackage** a System. String objektum példányait adja eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Átméretezés-AzureRmVirtualNetworkGateway](./Resize-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayVpnClientConfig](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


