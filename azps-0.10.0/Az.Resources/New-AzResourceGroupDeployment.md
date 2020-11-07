---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 35741c908e57e96fd4d9709ff350ac885f41181d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843326"
---
# New-AzResourceGroupDeployment

## Áttekintés
Azure-bevezetést ad hozzá egy erőforrás-csoporthoz.

## SZINTAXISA

### ByTemplateFileWithNoParameters (alapértelmezett)
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateFileAndParameterObject
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateUriAndParameterObject
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateFileAndParameterFile
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateUriAndParameterFile
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateFileAndParameterUri
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateUriAndParameterUri
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTemplateUriWithNoParameters
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzResourceGroupDeployment** parancsmag egy meglévő erőforráscsoport bevezetését adja eredményül.
Ez a beállítás tartalmazza a telepítéshez szükséges erőforrásokat.
Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis, webhely, virtuális gép vagy tárolási fiók.
Az Azure-erőforráscsoport olyan Azure-erőforrások gyűjteménye, amelyek egységként vannak telepítve, például a webhelyen, az adatbázis-kiszolgálón és a pénzügyi webhelyhez szükséges adatbázisokban.
Az erőforráscsoport-telepítés sablon használatával erőforrásokat ad hozzá egy erőforráscsoport számára, és közzéteszi őket, hogy azok elérhetők legyenek az Azure-ban.
Ha nem sablon nélkül szeretne erőforrásokat hozzáadni az erőforrás csoporthoz, használja az New-AzResource parancsmagot.
Erőforráscsoport-telepítő hozzáadásához adja meg egy meglévő erőforráscsoport és egy erőforráscsoport-sablon nevét.
Egy erőforráscsoport-sablon egy olyan JSON karakterlánc, amely egy komplex felhőalapú szolgáltatás erőforráscsoport, például egy webportál.
A sablon tartalmazza a paraméterek helyőrzőit a szükséges erőforrások és a konfigurálható tulajdonságértékek (például nevek és méretek) esetében.
Az Azure template gyűjteményben számos sablon található, vagy saját sablonokat is létrehozhat.
Sablon kereséséhez használhatja a **Get-AzResourceGroupGalleryTemplate** parancsmagot a gyűjteményben.
Ha egyéni sablont szeretne használni egy erőforráscsoport létrehozásához, adja meg a *TemplateFile* paramétert vagy a *TemplateUri* paramétert.
Mindegyik sablon rendelkezik a konfigurálható tulajdonságokra vonatkozó paraméterekkel.
A sablon paramétereinek értékeinek megadásához adja meg a *TemplateParameterFile* paramétert vagy a *TemplateParameterObject* paramétert.
Azt is megteheti, hogy egy sablon megadásakor dinamikusan hozzáadja a parancsot a parancshoz.
Ha dinamikus paramétereket szeretne használni, írja be őket a parancssorba, vagy írjon be egy mínuszjelet (-) a paraméter jelzéséhez, és a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.
A parancssorba beírt sablon paraméterei felülbírálják a Template paraméteres objektum vagy fájl értékeit.

## Példák

### 1. példa: egyéni sablon és paraméteres fájl használata a központi telepítő létrehozásához
```
PS C:\>New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

A parancs létrehoz egy új üzembe állítást egy egyéni sablon és egy sablonfájl segítségével a lemezen.
A parancs a *TemplateFile* paramétert használva adja meg a sablont és a *TemplateParameterFile* paramétert egy paramétert és paramétert tartalmazó fájl megadásához.

## PARAMÉTEREK

### -ApiVersion
Az erőforrás-szolgáltató által támogatott API-verziót adja meg.
Az alapértelmezett verziótól eltérő verziót is megadhat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
A parancsmag futtatása a háttérben

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentDebugLogLevel
A Debug naplózási szintjét adja meg.
A paraméter elfogadható értékei a következők:
- RequestContent
- ResponseContent
- Minden
- Nincs

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Üzemmód
A telepítő üzemmódot adja meg. A paraméter elfogadható értékei a következők:
- Teljes
- Növekményes mód: az erőforrás-kezelő törli azokat az erőforrásokat, amelyek szerepelnek az erőforrás csoportban, a sablonban azonban nincs megadva. A növekményes módban az erőforrás-kezelő nem módosított erőforrásokat hagy az erőforrás csoportban, a sablonban azonban nem.

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A létrehozandó erőforráscsoport-példány nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A telepítendő erőforráscsoport nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RollBackDeploymentName
Ha az erőforrás csoportban az adott nevű névvel a sikeres telepítésre szeretne visszagörgetni, akkor ne használja a ha-RollbackToLastDeployment használatát.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RollbackToLastDeployment
Az erőforrás csoport utolsó sikeres telepítésére való visszagörgetéskor ne legyen megjelenni, ha-RollBackDeploymentName használja.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TemplateFile
A JSON-sablonfájl teljes elérési útját adja meg.
Ez lehet egy egyéni sablon vagy egy olyan sablon, amelyet JSON-fájlként mentenek, például a **Save-AzResourceGroupGalleryTemplate** parancsmag használatával.

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterFile
A sablon paramétereinek nevét és értékét tartalmazó JSON-fájl teljes elérési útját adja meg.
Ha egy sablon tartalmaz paramétereket, akkor a *TemplateParameterFile* paraméterrel vagy a *TemplateParameterObject* paraméterrel kell megadnia a paraméterek értékét.
Sablon megadásakor a program dinamikusan hozzáadja a sablon paramétereit a parancshoz.
A dinamikus paraméterek használatához írjon be egy mínuszjelet (-) a paraméter nevének jelzéséhez, majd a TAB billentyűvel lépjen a rendelkezésre álló paraméterek között.

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterObject
A Template paraméterek neveinek és értékeinek hash-táblázatát adja meg.
Ha segítségre van szüksége a kivonatoló táblázatokhoz a Windows PowerShellben, írja be a következőt `Get-Help about_Hash_Tables` .
Ha egy sablonnak vannak paraméterei, meg kell adnia a paraméter értékét.
Sablon megadásakor a program dinamikusan hozzáadja a sablon paramétereit a parancshoz.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterUri
A sablon paramétereinek fájljának URI-azonosítóját adja meg.

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateUri
A JSON sablonfájl URI-jét adja meg.
Ez a fájl lehet egy egyéni sablon vagy egy JSON-fájlként mentett gyűjtemény-sablon, például a **Save-AzResourceGroupGalleryTemplate** használatával.

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. ResourceManager. models. PSResourceGroupDeployment

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzResourceGroupDeployment](./Get-AzResourceGroupDeployment.md)

[Új – AzResource](./New-AzResource.md)

[Új – AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Stop-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Teszt-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)


