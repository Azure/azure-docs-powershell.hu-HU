---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 5fb8c8f71366dd9fd0a2c6b12fc023c1ce3ccf9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502559"
---
# Update-AzureRmMlWebService

## Áttekintés
Meglévő webszolgáltatás-erőforrás tulajdonságainak frissítése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### UpdateFromParameters
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpdateFromObject
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az Update-AzureRmMlWebService parancsmag segítségével frissítheti egy webszolgáltatás nem statikus tulajdonságait.
A parancsmag a javítás műveletként működik.
Csak azokat a tulajdonságokat adja át, amelyeket módosítani szeretne.

## Példák

### --------------------------Példa 1: szelektív frissítési argumentumok--------------------------
```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

Itt cseréljük le a leírás, az elsődleges hozzáférés kulcsát, és engedélyeznie kell a diagnosztikai gyűjteményt minden nyomkövetéskor a webszolgáltatás futási időszaka alatt.

### --------------------------Példa 2: frissítés webszolgáltatás-példányon alapuló--------------------------
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

A példa először létrehoz egy webszolgáltatás-definíciót, amely csak a frissítendő mezőket tartalmazza, majd a Update-AzureRmMlWebService kéri, hogy alkalmazza őket a ServiceUpdates paraméter használatával.

## PARAMÉTEREK

### -Eszközök
A webszolgáltatást alkotó eszközök (például modulok, adatkészletek).

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Leírás
A webszolgáltatás leírásának új értéke.
Ez látható a szolgáltatás hencegő API-sémájában.

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Diagnosztika
A webszolgáltatás diagnosztikai nyomkövetési gyűjteményét szabályozó beállítások.

```yaml
Type: DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Ne kérjen megerősítést.

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

### – Bemenet
A webszolgáltatás bemenetének (ek) definíciója, a hencegő séma-konstrukcióban.

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsReadOnly
Megadja, hogy ez a webszolgáltatás írásvédett.
Miután beállította, a webszolgáltatás már nem frissíthető, többek között a tulajdonság értékének módosítása, és csak törölhető.

```yaml
Type: SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Billentyűk
A hívásoknak a szolgáltatás futásidejű API-khoz való hitelesítéséhez használt két hozzáférési kulcs (vagy mindkettő) frissítése

```yaml
Type: WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A frissítendő webszolgáltatás-erőforrás neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Output (kimenet)
A webszolgáltatás kimenetének (s) definíciója, a hencegő séma-konstrukcióban.

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Package (csomag)
A webszolgáltatás definiálására szolgáló Graph-csomag definíciója.

```yaml
Type: GraphPackage
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Paraméterek
A webes szolgáltatáshoz definiált globális paraméterek értéke, a globális paraméter neve – \> alapértelmezett érték gyűjtemény.
Ha nincs megadva alapértelmezett érték, akkor a paraméter szükségesnek tekintendő.

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RealtimeConfiguration
A szolgáltatás valósidejű végpontjának konfigurációjának frissítései.

```yaml
Type: RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A frissítendő webszolgáltatás a frissítendő webszolgáltatást tartalmazó erőforráscsoport.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceUpdates
Egy webszolgáltatás-definíciós példányként elérhető webszolgáltatásra érvényes módosítások halmaza.
Csak a nem statikus mezők módosulnak.

```yaml
Type: WebService
Parameter Sets: UpdateFromObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountKey
Elforgatja a webszolgáltatáshoz társított tárterület elérési útjának elérési kulcsát.

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cím
A webszolgáltatás címének új értéke.
Ez látható a szolgáltatás hencegő API-sémájában.

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### WebService
A ' ServiceUpdates ' paraméter a "webszolgáltatás" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás
Az Azure Machine learning webszolgáltatás összefoglaló leírása.
Hasonló a visszaadott leíráshoz, ha az Get-AzureRmMlWebService parancsmagot egy meglévő webszolgáltatásban hívja fel.
Ez a leírás nem tartalmaz bizalmas tulajdonságokat, például a tárolási fiók hitelesítő adatait és a szolgáltatás elérési kulcsait.

## MEGJEGYZI
Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml

## KAPCSOLÓDÓ HIVATKOZÁSOK

