---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015741"
---
# Stop-AzureVM

## Áttekintés
Egy Azure Virtual Machine leállása.

## SZINTAXISA

### ByName (alapértelmezett)
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Beviteli
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
A **stop-AzureVM** parancsmag leállítja a virtuális gépet.

## Példák

### Példa 1: virtuális gép leállítása
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

Ez a parancs leállítja a megadott szolgáltatás által használt virtuális gépet.

### 2. példa: virtuális gép leállítása egy virtuálisgép-objektum segítségével
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

Ez a parancs leállítja azt a virtuális gépet, amelyet a megadott szolgáltatás tartalmaz, a **beolvasás AzureVM** visszaadó virtuálisgép-objektum használatával.

### 3. példa: állítsa le a VM-et, és őrizze meg a VM kiépített változatát
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

Ez a parancs leállítja azt a virtuális gépet, amelyet a megadott szolgáltatás tartalmaz, és kiépített állapotban tartja.

### 4. példa: állítsa le a VM-et, és engedélyezze az utolsó VM kiosztását a központi üzembe helyezésben.
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

Ez a parancs leállítja azt a virtuális gépet, amelyet a megadott szolgáltatás tartalmaz, és lehetővé teszi az utolsó virtuális gép deallokációját a központi üzembe helyezéshez.

### Példa 5: több VMs kikapcsolása
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

Ez a parancs több olyan virtuális gépet leállít le, amelyeket a megadott szolgáltatás tartalmaz.

## PARAMÉTEREK

### -Force
Azt adja meg, hogy engedélyezi-e az utolsó virtuális gép deallokációját egy központi példányban.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
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

### -Name (név)
A leállításhoz a virtuális gép nevét adja meg.

A helyettesítő karakterrel több virtuális gépet aszinkron módon állíthat be.
A helyettesítő karakterekkel ez a parancsmag a leállítási szerepkörök https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx műveletét hívja le ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) a leállítási szerepkör https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx művelete helyett https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) ).

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Szolgáltatásnév
Annak a virtuális gépet tartalmazó Azure-szolgáltatásnak a neve, amelyről le kell állítani.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StayProvisioned
Megadja, hogy ez a parancsmag a virtuális gépet kiépítve tartja.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Olyan virtuálisgép-objektumot ad meg, amely azonosítja a virtuális gépet a leállításhoz.

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureVM](./Get-AzureVM.md)

[Új – AzureVM](./New-AzureVM.md)

[Újraindítás – AzureVM](./Restart-AzureVM.md)

[Start-AzureVM](./Start-AzureVM.md)


