---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017351"
---
# Set-AzureVMDscExtension

## Áttekintés
A DSC bővítmény beállítása virtuális gépen.

## SZINTAXISA

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureVMDscExtension** parancsmag a kívánt állapot-konfiguráció (DSC) kiterjesztését egy virtuális gépen állítja be.

## Példák

### 1. példa: a DSC-bővítmény beállítása virtuális gépen
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

Ez a parancs a DSC bővítményt egy virtuális gépen állítja be.

A MyConfiguration.ps1.zip csomagot előzőleg az Azure-tárhelyre kell feltölteni a **Közzététel – AzureVMDscConfiguration** parancs segítségével, és az MyConfiguration.ps1 parancsfájlt és az attól függ, hogy milyen modulokat tartalmaz.

A MyConfiguration argumentum az adott DSC-konfigurációt jelzi a végrehajtandó parancsfájlon belül.
A- *ConfigurationArgument* paraméter a konfigurációs függvénynek átadott argumentumokat tartalmazó Hashtable ad meg.

### 2. példa: a DSC-bővítmény konfigurálása virtuális gépen a konfigurációs adatokat tartalmazó útvonal használatával
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

Ez a parancs a DSC bővítményt egy virtuális gépen a konfigurációs adatelérési út segítségével állítja be.

## PARAMÉTEREK

### -ConfigurationArchive
Annak a konfigurációs csomagnak (. zip fájlnak) a nevét adja meg, amelyet korábban a közzététel – AzureVMDscConfiguration feltöltött.
Ehhez a paraméterhez csak a fájl nevét kell megadni elérési út nélkül.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationArgument
A konfigurációs függvény argumentumait megadó Hashtable adja meg.
A kulcsok megfelelnek a paraméterek neveinek és a paraméter értékeinek.

A paraméter elfogadható értékei a következők:

- primitív típusok
- karakterlánc
- tömb
- PSCredential

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Annak a. psd1 fájlnak az elérési útját adja meg, amely a konfigurációs függvény adatát adja meg.
Ennek a fájlnak a konfigurációs és környezeti adatainak elkülönítése című témakörben leírtak szerint tartalmaznia kell egy Hashtable https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationName
A DSC bővítmény által kezdeményezett konfigurációs parancsfájl vagy modul nevét adja meg.

Ennek a paraméternek az értékének a *ConfigurationArchive* -ban csomagolt parancsfájlokban vagy modulokban található egyik konfigurációs függvény nevének kell lennie.

Ez a parancsmag alapértelmezés szerint a *ConfigurationArchive* paraméter által megadott fájl nevét adja meg, ha ezt a paramétert kihagyja a kiterjesztés nélkül.
Ha például a *ConfigurationArchive* "SalesWebSite.ps1.zip", a *ConfigurationName* alapértelmezett értéke "SalesWebSite".

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContainerName
Annak az Azure-tárolónak a nevét adja meg, ahol a *ConfigurationArchive* található.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataCollection
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Jelzi, hogy ez a parancsmag felülírja a meglévő Blobs-objektumokat.

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

### -Hivatkozásnév
Olyan felhasználó által definiált karakterláncot ad meg, amely a kiterjesztésre hivatkozik.
Ezt a paramétert akkor adja meg a program, ha a bővítményt első alkalommal felveszi a virtuális gépre.
A későbbi frissítésekhez a bővítmény frissítésekor meg kell adnia a korábban használt hivatkozási nevet.
A bővítményhez rendelt *hivatkozásnév* a **Get-AzureVM** parancsmag használatával kapja.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
Itt adhatja meg a konfigurációs parancsfájl eléréséhez használt biztonsági beállításokat tartalmazó Azure Storage Context-környezetet.
Ez a környezet olvasási hozzáférést biztosít a *ContainerName* paraméter által megadott tárolóhoz.

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
Az összes tárolási szolgáltatás (például "core.contoso.net") DNS-végpontjának utótagját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Verzió
A DSC bővítmény adott verzióját adja meg.
Ha ez a paraméter nincs megadva, az alapértelmezett érték az "1. *" értékre van állítva.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Az állandó virtuálisgép-objektumot adja meg.

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

### -WmfVersion
A Windows Management Framework (WMF) verziószámát adja meg a virtuális gépre való telepítéshez.
A DSC bővítmény az olyan DSC-funkcióktól függ, amelyek csak a WMF frissítéseiben érhetők el.
Ez a paraméter adja meg, hogy a frissítés melyik verziójára telepítse a virtuális gépet.
A paraméter elfogadható értékei a következők:

- 4,0-ban.
A WMF 4,0 telepítése csak akkor, ha már telepítve van egy újabb verzió.
- 5,0-ban.
A WMF 5,0 legújabb verziójának telepítése.
- legújabb.
A legújabb WMF, jelenleg WMF 5,0 telepítése.

Az alapértelmezett érték a legújabb.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureVMDscExtension](./Get-AzureVMDscExtension.md)

[Remove-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[Remove-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[Get-AzureVM](./Get-AzureVM.md)

[Közzététel – AzureVMDscConfiguration](./Publish-AzureVMDscConfiguration.md)


