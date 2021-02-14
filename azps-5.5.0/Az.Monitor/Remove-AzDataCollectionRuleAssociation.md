---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 798bb97b9e84121894341dd807bbaa9b3658a039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203404"
---
# <span data-ttu-id="5d9d0-101">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="5d9d0-101">Remove-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="5d9d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d9d0-102">SYNOPSIS</span></span>
<span data-ttu-id="5d9d0-103">Adatgyűjtési szabály társításának törlése</span><span class="sxs-lookup"><span data-stu-id="5d9d0-103">Delete a data collection rule association.</span></span>

## <span data-ttu-id="5d9d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d9d0-104">SYNTAX</span></span>

### <span data-ttu-id="5d9d0-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d9d0-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -TargetResourceId <string> 
      -AssociationName <string> 
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="5d9d0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5d9d0-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="5d9d0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d9d0-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="5d9d0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d9d0-108">DESCRIPTION</span></span>
<span data-ttu-id="5d9d0-109">A **Remove-AzDataCollectionRuleAssociation** parancsmag töröl egy adatgyűjtési szabály társítását (DCRA).</span><span class="sxs-lookup"><span data-stu-id="5d9d0-109">The **Remove-AzDataCollectionRuleAssociation** cmdlet delete a data collection rule association (DCRA).</span></span>

<span data-ttu-id="5d9d0-110">DCR virtuális gépre való alkalmazáshoz társítást kell létrehoznia a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="5d9d0-110">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="5d9d0-111">Előfordulhat, hogy egy virtuális gép több DKR-hez kapcsolódik, és a DCR-hez több virtuális gép is társítva lehet.</span><span class="sxs-lookup"><span data-stu-id="5d9d0-111">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="5d9d0-112">Ez lehetővé teszi, hogy definiálja a tartományvezérlők készletét, amelyek mindegyikének meg kell egyeztetnie egy bizonyos követelményt, és csak azokra a virtuális gépekre alkalmazza őket, amelyekre vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="5d9d0-112">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="5d9d0-113">Az alábbi "Adatgyűjtés konfigurálása az [Azure Monitor-ügynökhöz"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) a DCRA-cikk alapján olvasható.</span><span class="sxs-lookup"><span data-stu-id="5d9d0-113">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="5d9d0-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d9d0-114">EXAMPLES</span></span>

### <span data-ttu-id="5d9d0-115">1. példa: Az adatgyűjtési szabályok társításának törlése névvel és célerőforrás-azonosítóval (társított virtuális gép) paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="5d9d0-115">Example 1: Delete data collection rule association with name and target resource ID (associated virtual machine) parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### <span data-ttu-id="5d9d0-116">2. példa: Adatgyűjtési szabály törlése bemeneti objektummal</span><span class="sxs-lookup"><span data-stu-id="5d9d0-116">Example 2: Delete data collection rule with Input Object</span></span>
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### <span data-ttu-id="5d9d0-117">3. példa: Adatgyűjtési szabály törlése a társítási erőforrás-azonosító tulajdonsággal</span><span class="sxs-lookup"><span data-stu-id="5d9d0-117">Example 3: Delete data collection rule with the association resource ID property</span></span>
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## <span data-ttu-id="5d9d0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d9d0-118">PARAMETERS</span></span>

### <span data-ttu-id="5d9d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d9d0-119">-DefaultProfile</span></span>
<span data-ttu-id="5d9d0-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5d9d0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d9d0-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="5d9d0-121">-TargetResourceId</span></span>
<span data-ttu-id="5d9d0-122">A társított erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5d9d0-122">The associated resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9d0-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="5d9d0-123">-AssociationName</span></span>
<span data-ttu-id="5d9d0-124">A társítási erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5d9d0-124">The name of the association resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName (Default)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9d0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d9d0-125">-InputObject</span></span>
<span data-ttu-id="5d9d0-126">PSDataCollectionRuleResource objektum</span><span class="sxs-lookup"><span data-stu-id="5d9d0-126">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="5d9d0-127">-AssociationId</span><span class="sxs-lookup"><span data-stu-id="5d9d0-127">-AssociationId</span></span>
<span data-ttu-id="5d9d0-128">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5d9d0-128">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9d0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d9d0-129">-Confirm</span></span>
<span data-ttu-id="5d9d0-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5d9d0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d9d0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d9d0-131">-WhatIf</span></span>
<span data-ttu-id="5d9d0-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5d9d0-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d9d0-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d9d0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d9d0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d9d0-134">CommonParameters</span></span>
<span data-ttu-id="5d9d0-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d9d0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d9d0-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d9d0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d9d0-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d9d0-137">INPUTS</span></span>

### <span data-ttu-id="5d9d0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5d9d0-138">System.String</span></span>
###<span data-ttu-id="5d9d0-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="5d9d0-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="5d9d0-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d9d0-140">OUTPUTS</span></span>

### <span data-ttu-id="5d9d0-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d9d0-141">System.Boolean</span></span>

## <span data-ttu-id="5d9d0-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d9d0-142">NOTES</span></span>

## <span data-ttu-id="5d9d0-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d9d0-143">RELATED LINKS</span></span>

<span data-ttu-id="5d9d0-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="5d9d0-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span></span>
