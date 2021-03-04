---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 1a63d28664eb8ade22c87cfad3a21db0764cbceb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932650"
---
# <span data-ttu-id="40cbf-101">Get-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="40cbf-101">Get-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="40cbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40cbf-102">SYNOPSIS</span></span>
<span data-ttu-id="40cbf-103">Adatgyűjtési szabályok társítását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="40cbf-103">Gets data collection rule association(s).</span></span>

## <span data-ttu-id="40cbf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="40cbf-104">SYNTAX</span></span>

### <span data-ttu-id="40cbf-105">ByAssociatedResource (Default)</span><span class="sxs-lookup"><span data-stu-id="40cbf-105">ByAssociatedResource (Default)</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="40cbf-106">ByName</span><span class="sxs-lookup"><span data-stu-id="40cbf-106">ByName</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   -AssociationName <string> 
   [-DefaultProfile <IAzureContextContainer>] 
   [<CommonParameters>]
```

### <span data-ttu-id="40cbf-107">ByRule</span><span class="sxs-lookup"><span data-stu-id="40cbf-107">ByRule</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="40cbf-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="40cbf-108">ByInputObject</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="40cbf-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="40cbf-109">DESCRIPTION</span></span>
<span data-ttu-id="40cbf-110">A **Get-AzDataCollectionRuleAssociation** parancsmag egy vagy több adatgyűjtési szabály társítást kap (DCRA).</span><span class="sxs-lookup"><span data-stu-id="40cbf-110">The **Get-AzDataCollectionRuleAssociation** cmdlet gets one or more data collection rules associations (DCRA).</span></span>

<span data-ttu-id="40cbf-111">DCR virtuális gépre való alkalmazáshoz társítást kell létrehoznia a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="40cbf-111">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="40cbf-112">Előfordulhat, hogy egy virtuális gép több DKR-hez kapcsolódik, és a DCR-hez több virtuális gép is társítva lehet.</span><span class="sxs-lookup"><span data-stu-id="40cbf-112">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="40cbf-113">Ez lehetővé teszi, hogy definiálja a tartományvezérlők készletét, amelyek mindegyikének meg kell egyeztet egy bizonyos követelményt, és csak azokra a virtuális gépekre alkalmazza őket, amelyekre vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="40cbf-113">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="40cbf-114">Az alábbi "Adatgyűjtés konfigurálása az [Azure Monitor-ügynökhöz"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) a DCRA-cikk alapján olvasható.</span><span class="sxs-lookup"><span data-stu-id="40cbf-114">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="40cbf-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="40cbf-115">EXAMPLES</span></span>

### <span data-ttu-id="40cbf-116">1. példa: Adatgyűjtési szabályok társításának lekérte célerőforrás-azonosító szerint (társított virtuális gép)</span><span class="sxs-lookup"><span data-stu-id="40cbf-116">Example 1: Get data collection rules associations by target resource ID (associated virtual machine)</span></span>
```
PS C:\>$vm = Get-AzVM -ResourceGroupName $rg -Name $vmName
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="40cbf-117">Ez a parancs felsorolja az adott célerőforrás-azonosító (virtuális gép) adatgyűjtési szabályait.</span><span class="sxs-lookup"><span data-stu-id="40cbf-117">This command lists all the data collection rules for the given target resource ID (virtual machine).</span></span>

### <span data-ttu-id="40cbf-118">2. példa: Adatgyűjtési szabályok társításának begyűjtése szabály szerint (DCR)</span><span class="sxs-lookup"><span data-stu-id="40cbf-118">Example 2: Get data collection rules associations by rule (DCR)</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -ResourceGroup $rg -RuleName $dcrName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="40cbf-119">Ez a parancs felsorolja az adott erőforráscsoporthoz és -szabályhoz (DCR) vonatkozó adatgyűjtési szabályok társítását.</span><span class="sxs-lookup"><span data-stu-id="40cbf-119">This command lists data collection rules associations for the given resource group and rule (DCR).</span></span>

### <span data-ttu-id="40cbf-120">3. példa: Adatgyűjtési szabály-társítások begyűjtése bemeneti objektum alapján (PSDataCollectionRuleResource)</span><span class="sxs-lookup"><span data-stu-id="40cbf-120">Example 3: Get data collection rule associations by input object (PSDataCollectionRuleResource)</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$dcr | Get-AzDataCollectionRuleAssociation

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="40cbf-121">Ez a parancs felsorolja az adott bemeneti objektum adatgyűjtési szabályok társítását.</span><span class="sxs-lookup"><span data-stu-id="40cbf-121">This command lists data collection rules associations for the given input object.</span></span>

### <span data-ttu-id="40cbf-122">4. példa: Adatgyűjtési szabály társítása célerőforrás-azonosító (társított virtuális gép) és társítás neve alapján</span><span class="sxs-lookup"><span data-stu-id="40cbf-122">Example 4: Get a data collection rule association by target resource ID (associated virtual machine) and association name</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="40cbf-123">Ez a parancs felsorol egy (egy elemet tartalmazó listát) az adatgyűjtési szabályok társításával.</span><span class="sxs-lookup"><span data-stu-id="40cbf-123">This command lists one (a list with a single element) data collection rule association.</span></span>

## <span data-ttu-id="40cbf-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40cbf-124">PARAMETERS</span></span>

### <span data-ttu-id="40cbf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40cbf-125">-DefaultProfile</span></span>
<span data-ttu-id="40cbf-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="40cbf-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40cbf-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="40cbf-127">-TargetResourceId</span></span>
<span data-ttu-id="40cbf-128">A társított erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="40cbf-128">The associated resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByAssociatedResource (Default)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="40cbf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40cbf-129">-ResourceGroupName</span></span>
<span data-ttu-id="40cbf-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="40cbf-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cbf-131">-RuleName</span><span class="sxs-lookup"><span data-stu-id="40cbf-131">-RuleName</span></span>
<span data-ttu-id="40cbf-132">Az adatgyűjtési szabály neve</span><span class="sxs-lookup"><span data-stu-id="40cbf-132">The data collection rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases: DataCollectionRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cbf-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40cbf-133">-InputObject</span></span>
<span data-ttu-id="40cbf-134">PSDataCollectionRuleResource objektum</span><span class="sxs-lookup"><span data-stu-id="40cbf-134">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="40cbf-135">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="40cbf-135">-AssociationName</span></span>
<span data-ttu-id="40cbf-136">A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="40cbf-136">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cbf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40cbf-137">CommonParameters</span></span>
<span data-ttu-id="40cbf-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40cbf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40cbf-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40cbf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40cbf-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40cbf-140">INPUTS</span></span>

### <span data-ttu-id="40cbf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="40cbf-141">System.String</span></span>
### <span data-ttu-id="40cbf-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="40cbf-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="40cbf-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40cbf-143">OUTPUTS</span></span>

### <span data-ttu-id="40cbf-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="40cbf-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="40cbf-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="40cbf-145">NOTES</span></span>

## <span data-ttu-id="40cbf-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40cbf-146">RELATED LINKS</span></span>

<span data-ttu-id="40cbf-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="40cbf-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span></span>
