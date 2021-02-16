---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: b174fdec51ece178b2e49a8e6e33d1e74f62c61f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402439"
---
# <span data-ttu-id="f2a2d-101">New-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="f2a2d-101">New-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="f2a2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a2d-103">Adatgyűjtési szabály társításának létrehozása</span><span class="sxs-lookup"><span data-stu-id="f2a2d-103">Create data collection rule association.</span></span>

## <span data-ttu-id="f2a2d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2a2d-104">SYNTAX</span></span>

### <span data-ttu-id="f2a2d-105">ByDataCollectionRuleId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2a2d-105">ByDataCollectionRuleId (Default)</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -RuleId <string>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="f2a2d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f2a2d-106">ByInputObject</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -InputObject <PSDataCollectionRuleResource>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]  
   [-WhatIf]   
   [-Confirm]   
   [<CommonParameters>]
```


## <span data-ttu-id="f2a2d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2a2d-107">DESCRIPTION</span></span>
<span data-ttu-id="f2a2d-108">A **New-AzDataCollectionRuleAssociation** parancsmag létrehoz egy adatgyűjtési szabályok társítását (DCRA).</span><span class="sxs-lookup"><span data-stu-id="f2a2d-108">The **New-AzDataCollectionRuleAssociation** cmdlet creates a data collection rules association (DCRA).</span></span>

<span data-ttu-id="f2a2d-109">DCR virtuális gépre való alkalmazáshoz társítást kell létrehoznia a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="f2a2d-109">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="f2a2d-110">Előfordulhat, hogy egy virtuális gép több DKR-hez kapcsolódik, és a DCR-hez több virtuális gép is társítva lehet.</span><span class="sxs-lookup"><span data-stu-id="f2a2d-110">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="f2a2d-111">Ez lehetővé teszi, hogy definiálja a tartományvezérlők készletét, amelyek mindegyikének meg kell egyeztet egy bizonyos követelményt, és csak azokra a virtuális gépekre alkalmazza őket, amelyekre vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="f2a2d-111">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="f2a2d-112">Az alábbi "Adatgyűjtés konfigurálása az [Azure Monitor-ügynökhöz"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) a DCRA-cikk alapján olvasható.</span><span class="sxs-lookup"><span data-stu-id="f2a2d-112">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="f2a2d-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2a2d-113">EXAMPLES</span></span>

### <span data-ttu-id="f2a2d-114">1. példa: Adatgyűjtési szabály társításának létrehozása</span><span class="sxs-lookup"><span data-stu-id="f2a2d-114">Example 1: Create data collection rule association</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssoc" -RuleId $dcr.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssoc
Name                 : dcrAssoc
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="f2a2d-115">Ez a parancs egy adatgyűjtési szabály társítását hozza létre az adott szabályhoz és célerőforrás-azonosítóhoz.</span><span class="sxs-lookup"><span data-stu-id="f2a2d-115">This command creates a data collection rule association for given rule and target resource ID.</span></span>

### <span data-ttu-id="f2a2d-116">2. példa: Adatgyűjtési szabály társítása DCR-objektumból</span><span class="sxs-lookup"><span data-stu-id="f2a2d-116">Example 2: Create data collection rule association from a DCR object</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>$dcr | New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssocInput"

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssocInput
Name                 : dcrAssocInput
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="f2a2d-117">Ez a parancs egy adatgyűjtési szabály társítását hozza létre az adott szabályhoz és célerőforrás-azonosítóhoz.</span><span class="sxs-lookup"><span data-stu-id="f2a2d-117">This command creates a data collection rule association for given rule and target resource ID.</span></span>

## <span data-ttu-id="f2a2d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2a2d-118">PARAMETERS</span></span>

### <span data-ttu-id="f2a2d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a2d-119">-DefaultProfile</span></span>
<span data-ttu-id="f2a2d-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f2a2d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2a2d-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f2a2d-121">-TargetResourceId</span></span>
<span data-ttu-id="f2a2d-122">A társítani szükséges erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="f2a2d-122">The resource ID to associate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a2d-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="f2a2d-123">-AssociationName</span></span>
<span data-ttu-id="f2a2d-124">Az erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="f2a2d-124">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a2d-125">-RuleId</span><span class="sxs-lookup"><span data-stu-id="f2a2d-125">-RuleId</span></span>
<span data-ttu-id="f2a2d-126">Az adatgyűjtési szabály azonosítója</span><span class="sxs-lookup"><span data-stu-id="f2a2d-126">The data collection rule ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByDataCollectionRuleId
Aliases: DataCollectionRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a2d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2a2d-127">-InputObject</span></span>
<span data-ttu-id="f2a2d-128">PSDataCollectionRuleResource objektum</span><span class="sxs-lookup"><span data-stu-id="f2a2d-128">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="f2a2d-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f2a2d-129">-Description</span></span>
<span data-ttu-id="f2a2d-130">Az erőforrás leírása</span><span class="sxs-lookup"><span data-stu-id="f2a2d-130">The resource description</span></span>

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

### <span data-ttu-id="f2a2d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2a2d-131">-Confirm</span></span>
<span data-ttu-id="f2a2d-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f2a2d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2a2d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2a2d-133">-WhatIf</span></span>
<span data-ttu-id="f2a2d-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f2a2d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2a2d-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f2a2d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2a2d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a2d-136">CommonParameters</span></span>
<span data-ttu-id="f2a2d-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2a2d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a2d-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2a2d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a2d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2a2d-139">INPUTS</span></span>

### <span data-ttu-id="f2a2d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f2a2d-140">System.String</span></span>

## <span data-ttu-id="f2a2d-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2a2d-141">OUTPUTS</span></span>

### <span data-ttu-id="f2a2d-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="f2a2d-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="f2a2d-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2a2d-143">NOTES</span></span>

## <span data-ttu-id="f2a2d-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2a2d-144">RELATED LINKS</span></span>

<span data-ttu-id="f2a2d-145">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="f2a2d-145">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span></span>
