---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301073"
---
# Get-AzTemplateSpec

## Áttekintés
Sablonok specifikációjának beolvasása vagy listázása

## SZINTAXISA

### ListTemplateSpecsParameterSet (alapértelmezett)
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetTemplateSpecByNameParameterSet
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetTemplateSpecByIdParameterSet
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Ez a parancsmag használható az előfizetésben/erőforrás csoportban lévő sablon specifikációjának listázására, illetve egy adott sablon specifikációjának vagy azonosítójának beszerzésére. Ha egy adott verziót egy adott verzióval egy adott verzióval egy adott verzióra, akkor a verziószámot a **verziószám paraméterrel** kell megadnia. A **verzió** használatakor a program csak az adott verzió részleteit fogja tartalmazni a *-ban *.* A visszaadott sablon spec objektumának verziószáma. Ha nem ad meg konkrét verziót, ha a sablont egy név vagy azonosító szerint adja meg, akkor minden verzió megtalálható lesz a * címen *.* A visszaadott objektum verziói tulajdonsága.

**Megjegyzés** : Ha az előfizetésben vagy az erőforrás csoportban található minden sablonra vonatkozó specifikációt ad meg, a program minden olyan sablont ad vissza *. A Versions* tulajdonság *értéke null* lesz. A verziós adatok csak akkor jelennek meg, ha-Name vagy-ResourceId paramétereket tartalmaz (például: egy adott sablont kér a spec/Version).

## Példák

### 1. példa: a lista sablon specifikációi a jelenlegi előfizetésben
```powershell
PS C:\> Get-AzTemplateSpec
```

Felsorolja az összes sablon specifikációját a jelenlegi előfizetésben.

### 2. példa: egy erőforráscsoport lista sablon specifikációja
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Felsorolja az összes sablon specifikációját az aktuális előfizetés erőforráscsoport "myRG" csoportjában.

### 3. példa: a sablon specifikációjának beszerzése (minden verzióval) név szerint
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Információt kap a "MyTemplateSpec" nevű "myRG" erőforráscsoporthoz tartozó "" nevű sablonról.

**Megjegyzés** : az összes sablon specifikációjának verziószáma a következő lesz: " *.* A feladó objektum verzió tulajdonsága.

### Példa 4: a sablon specifikációjának beszerzése (adott verzió) név szerint
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Információt kap a ' MyTemplateSpec ' nevű "myRG" erőforráscsoporthoz tartozó "" nevű sablon "v 1.0" verziójáról.

**Megjegyzés** : a *".* A visszaadott objektum (verziók) tulajdonsága csak a kért verziót fogja tartalmazni.

### Példa 5: erőforrás-azonosító lekérése a sablonhoz (minden verzióval)
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Információt kap az "MyTemplateSpec" nevű "" nevű sablonról az előfizetés subId erőforráscsoport "myRG" csoportjában \{ \} .

**Megjegyzés** : az összes sablon specifikációjának verziószáma a következő lesz: " *.* A feladó objektum verzió tulajdonsága.

### Példa 6: erőforrás-azonosító (adott verzió) beolvasása erőforrás-azonosítóval
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Információt kap az "MyTemplateSpec" nevű "myRG" nevű erőforráscsoport "v 1.0" verziójáról az előfizetés \{ subId \} .

**Megjegyzés** : a *".* A visszaadott objektum (verziók) tulajdonsága csak a kért verziót fogja tartalmazni.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Annak a sablonnak a neve, amely a spec nevet adja.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
A sablon teljes értékű erőforrás-azonosítója (példa:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName})

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Verzió
A sablon specifikációjának verziója.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSTemplateSpec

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
