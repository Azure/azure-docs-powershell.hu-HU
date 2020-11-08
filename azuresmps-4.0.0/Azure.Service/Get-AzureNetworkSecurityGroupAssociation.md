---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 6AF7D392-8C8B-4695-95D0-E927093F654A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21eb1b7bcad200e67659f830bfb3bbef42fe0f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016582"
---
# Get-AzureNetworkSecurityGroupAssociation

## Áttekintés
Egy virtuális gép, hálózati adapter vagy Péter szerepkör hálózati biztonsági csoportjának beolvasása

## SZINTAXISA

### GetNetworkSecurityGroupAssociationForSubnet
```
Get-AzureNetworkSecurityGroupAssociation -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GetNetworkSecurityGroupAssociationForIaaSRole
```
Get-AzureNetworkSecurityGroupAssociation -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GetNetworkSecurityGroupAssociationForPaaSRole
```
Get-AzureNetworkSecurityGroupAssociation [-Slot <String>] -RoleName <String> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureNetworkSecurityGroupAssociation** parancsmag a virtuális gép, hálózati adapter vagy platform hálózati biztonsági csoportjának szolgáltatás (Pásti) szerepkörét kapja.

## Példák

### Példa 1: a virtuális gép hálózati biztonsági csoportjának beszerzése
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureNetworkSecurityGroupAssociation
```

Ez a parancs egy ContosoVM06 nevű virtuális gépet kap a ContosoService nevű szolgáltatáshoz, és átadja a virtuális gép objektumát az aktuális parancsmagnak.
Az aktuális parancsmag a virtuális géphez társított hálózati biztonsági csoportot kapja meg.

## PARAMÉTEREK

### – Részletes
Azt jelzi, hogy ez a parancsmag a virtuális géphez társított hálózati biztonsági csoport adatait adja eredményül.
Ezek a részletek a hely és a szabályok között is szerepelnek.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkInterfaceName
Annak a hálózati adapternek a neve, amelyhez a parancsmag a hálózat biztonsági csoportját kapja.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható. Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName
Annak a Péter-szerepnek a nevét adja meg, amelyhez ez a parancsmag a hálózat biztonsági csoportját kapja.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szolgáltatásnév
Egy felhőalapú szolgáltatás nevét adja meg.
A Péter-szerep a paraméter által megadott szolgáltatáshoz tartozik.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
A Péter-bővítőhelyet adja meg.
A Pásti szerepkör, amelyhez a parancsmag a hálózati biztonsági csoportot kapja, a megfelelő bővítőhelyet adja meg.
Az érvényes értékek a következők: 

- Production
- Átmeneti tárolásra szolgáló 

Az alapértelmezett érték a termelés.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
Annak az alhálózatnak a neve, amelyhez a parancsmag a hálózat biztonsági csoportját kapja.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkName
Megadja annak a virtuális hálózatnak a nevét, amely tartalmazza azt az alhálózatot, amelynek a parancsmagja a hálózat biztonsági csoportját kapja.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Azt a virtuális gépet adja meg, amelyre a parancsmag a hálózat biztonsági csoportját alkalmazza.

```yaml
Type: PersistentVMRoleContext
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. WindowsAzure. Command. ServiceManagement. Network. NetworkSecurityGroup. Model. INetworkSecurityGroup

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzureNetworkSecurityGroupAssociation](./Remove-AzureNetworkSecurityGroupAssociation.md)

[Set-AzureNetworkSecurityGroupAssociation](./Set-AzureNetworkSecurityGroupAssociation.md)


