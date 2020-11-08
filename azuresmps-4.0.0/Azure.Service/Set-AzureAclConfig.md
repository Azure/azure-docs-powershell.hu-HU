---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016432"
---
# Set-AzureAclConfig

## Áttekintés
ACL-konfiguráció objektumának módosítása.

## SZINTAXISA

### AddRule
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### RemoveRule
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### SetRule
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **set-AzureAclConfig** parancsmag a hozzáférés-vezérlési listák (ACL) konfigurációs objektumait egy meglévő Azure Virtual Machine-konfigurációban módosítja.

## Példák

### 1. példa: szabály felvétele új ACL-konfigurációba
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

Az első parancs ACL-konfigurációt hoz létre, majd a $Acl változóban tárolja.

A második parancs új szabályt ad hozzá a $Aclban tárolt konfigurációhoz.
A parancs a szabály műveletét, alhálózatát, sorrendjét és leírását adja meg.

### 2. példa: szabály módosítása ACL-konfigurációban
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

Az első parancs a **Get-AzureVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban.
A parancs átadja az objektumot a **Get-AzureAclConfig** parancsmagnak a pipeline operátor használatával.
Ez a parancsmag a Web nevű végpont ACL-konfigurációját kapja meg.
A parancs az ACL konfigurációs objektumát az $Acl változóban tárolja.

A második parancs módosítja a 0 AZONOSÍTÓJÚ szabályt.
A parancs módosítja a szabály sorrendjét és leírását.

A végleges parancs a **set-AzureEndpoint** parancsmaggal beállítja a virtuális gép ACL-konfigurációs objektumát.
A parancs a virtuális gépet is frissíti.

### 3. példa: szabály eltávolítása ACL-konfigurációból
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

Az első parancs egy ACL-konfigurációs objektumot tárol a $Acl változóban.
Ugyanaz, mint az előző példában.

A második parancs eltávolítja a 0 AZONOSÍTÓJÚ szabályt az $Acl ACL-konfigurációjától.

A végleges parancs beállítja a virtuális gép ACL-konfigurációs objektumát, és frissíti a virtuális gépet.
Ugyanaz, mint az előző példában.

## PARAMÉTEREK

### -ACL
Olyan ACL-konfigurációs objektumot ad meg, amelyet a parancsmag módosított.

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Műveletek
A parancsmag által hozzáadott vagy módosított szabályra vonatkozó műveleteket adja meg.
Az érvényes értékek a következők: engedélyezés és megtagadás.

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRule
Jelzi, hogy ez a parancsmag szabályt ad az ACL-konfigurációhoz.

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Leírás
A parancsmag által hozzáadott vagy módosított szabály leírását adja meg.

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Order (rendelés)
A parancsmag által hozzáadott vagy módosított szabály feldolgozási sorrendjét adja meg.

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteSubnet
A parancsmag által hozzáadott vagy módosított szabály távoli alhálózatát adja meg.
Egy, az osztály nélküli tartományok közötti útválasztási (CIDR) formátumú címet adja meg.

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRule
Jelzi, hogy ez a parancsmag eltávolítja a szabályt az ACL-konfigurációból.

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleId
Annak a szabálynak az AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja vagy módosította az ACL-konfigurációt.

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetRule
Jelzi, hogy az adott parancsmag módosította az ACL-konfiguráció szabályait.

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureAclConfig](./Get-AzureAclConfig.md)

[Get-AzureVM](./Get-AzureVM.md)

[Új – AzureAclConfig](./New-AzureAclConfig.md)

[Remove-AzureAclConfig](./Remove-AzureAclConfig.md)

[Set-AzureEndpoint](./Set-AzureEndpoint.md)

[Update-AzureVM](./Update-AzureVM.md)


