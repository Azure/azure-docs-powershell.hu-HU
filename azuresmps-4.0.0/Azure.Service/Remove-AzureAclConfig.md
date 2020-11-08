---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 915CBA29-5A58-4A5D-9F02-976CB76D4800
online version: ''
schema: 2.0.0
ms.openlocfilehash: af98cbdc0be73c87682d0ed004d17cd9e82c9baa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016175"
---
# Remove-AzureAclConfig

## Áttekintés
ACL-konfigurációs objektum eltávolítása Azure Virtual Machine-konfigurációból.

## SZINTAXISA

```
Remove-AzureAclConfig [-EndpointName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureAclConfig** parancsmag eltávolítja a hozzáférés-vezérlési lista (ACL) konfigurációs objektumát egy Azure Virtual Machine-konfigurációból.

## Példák

### Példa 1: ACL-konfiguráció eltávolítása
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureAclConfig -EndpointName "Web" | Update-AzureVM
```

Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban.
A parancs a csővezeték-kezelő használatával továbbítja az objektumot az aktuális parancsmaghoz.
Ez a parancsmag eltávolítja a Web nevű végpont ACL-konfigurációját.
A parancs átadja az eredményt az **Update-AzureVM** parancsmagnak, amely frissíti a virtuális gépet.

## PARAMÉTEREK

### -EndpointName
Annak a végpontnak a neve, amelyből a parancsmag eltávolítja az ACL-konfigurációt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

### -VM
Azt a virtuális gépet adja meg, amelyből ez a parancsmag eltávolítja az ACL-konfigurációt.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

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

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureAclConfig](./Get-AzureAclConfig.md)

[Get-AzureVM](./Get-AzureVM.md)

[Új – AzureAclConfig](./New-AzureAclConfig.md)

[Set-AzureAclConfig](./Set-AzureAclConfig.md)

[Update-AzureVM](./Update-AzureVM.md)


