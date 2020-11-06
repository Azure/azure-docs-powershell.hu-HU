---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 0ba43a38763252275d7461f11cc4db574720ba5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498903"
---
# <span data-ttu-id="9e81c-101">New-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="9e81c-101">New-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="9e81c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e81c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e81c-103">Munkaterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9e81c-103">Creates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e81c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e81c-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e81c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e81c-105">DESCRIPTION</span></span>
<span data-ttu-id="9e81c-106">A **New-AzureRmOperationalInsightsWorkspace** parancsmag létrehoz egy munkaterületet a megadott erőforráscsoport és-hely között.</span><span class="sxs-lookup"><span data-stu-id="9e81c-106">The **New-AzureRmOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="9e81c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9e81c-107">EXAMPLES</span></span>

### <span data-ttu-id="9e81c-108">1. példa: munkaterület létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="9e81c-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="9e81c-109">Ez a parancs létrehoz egy MyWorkspace nevű szabványos SKU-munkaterületet az ContosoResourceGroup nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="9e81c-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="9e81c-110">2. példa: munkaterület létrehozása és csatolása meglévő fiókhoz</span><span class="sxs-lookup"><span data-stu-id="9e81c-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="9e81c-111">Az első parancs az Get-AzureRmOperationalInsightsLinkTargets parancsmagot használja az üzemeltetési statisztika-célok eléréséhez, majd a $OILinkTargets változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="9e81c-111">The first command uses the Get-AzureRmOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>

<span data-ttu-id="9e81c-112">A második parancs átadja az első fiók hivatkozás célját $OILinkTargets a **New-AzureRmOperationalInsightsWorkspace** parancsmagot a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="9e81c-112">The second command passes the first account link target in $OILinkTargets to the **New-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9e81c-113">A parancs létrehoz egy MyWorkspace nevű szabványos SKU-munkaterületet, amely a $OILinkTargets első üzemi betekintési fiókjához van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="9e81c-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="9e81c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e81c-114">PARAMETERS</span></span>

### <span data-ttu-id="9e81c-115">-Vevőkód</span><span class="sxs-lookup"><span data-stu-id="9e81c-115">-CustomerId</span></span>
<span data-ttu-id="9e81c-116">Azt a fiókot adja meg, amelyre a munkaterület hivatkozni fog.</span><span class="sxs-lookup"><span data-stu-id="9e81c-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="9e81c-117">A Get-AzureRmOperationalInsightsLinkTargets parancsmag a potenciális fiókok listázására is használható.</span><span class="sxs-lookup"><span data-stu-id="9e81c-117">The Get-AzureRmOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e81c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e81c-118">-DefaultProfile</span></span>
<span data-ttu-id="9e81c-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9e81c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e81c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9e81c-120">-Force</span></span>
<span data-ttu-id="9e81c-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9e81c-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e81c-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="9e81c-122">-Location</span></span>
<span data-ttu-id="9e81c-123">Azt a helyet adja meg, ahol létrehozhatja a munkaterületet (például kelet-amerikai vagy Nyugat-európai).</span><span class="sxs-lookup"><span data-stu-id="9e81c-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e81c-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e81c-124">-Name</span></span>
<span data-ttu-id="9e81c-125">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e81c-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="9e81c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e81c-126">-ResourceGroupName</span></span>
<span data-ttu-id="9e81c-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e81c-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9e81c-128">A munkaterület ebben az erőforráscsoportben jön létre.</span><span class="sxs-lookup"><span data-stu-id="9e81c-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="9e81c-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9e81c-129">-RetentionInDays</span></span>
<span data-ttu-id="9e81c-130">Munkaterület-adatmegőrzés napokban.</span><span class="sxs-lookup"><span data-stu-id="9e81c-130">The workspace data retention in days.</span></span> <span data-ttu-id="9e81c-131">a 730 napok az összes többi SKU számára megengedett maximális érték.</span><span class="sxs-lookup"><span data-stu-id="9e81c-131">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e81c-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="9e81c-132">-Sku</span></span>
<span data-ttu-id="9e81c-133">A munkaterület szolgáltatási rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e81c-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="9e81c-134">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="9e81c-134">Valid values are:</span></span> 

- <span data-ttu-id="9e81c-135">ingyenes</span><span class="sxs-lookup"><span data-stu-id="9e81c-135">free</span></span>
- <span data-ttu-id="9e81c-136">Standard</span><span class="sxs-lookup"><span data-stu-id="9e81c-136">standard</span></span>
- <span data-ttu-id="9e81c-137">prémium verzió</span><span class="sxs-lookup"><span data-stu-id="9e81c-137">premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e81c-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="9e81c-138">-Tag</span></span>
<span data-ttu-id="9e81c-139">A munkaterület erőforrás-címkéi.</span><span class="sxs-lookup"><span data-stu-id="9e81c-139">The resource tags for the workspace.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e81c-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9e81c-140">-Confirm</span></span>
<span data-ttu-id="9e81c-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9e81c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e81c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e81c-142">-WhatIf</span></span>
<span data-ttu-id="9e81c-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9e81c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e81c-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e81c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e81c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e81c-145">CommonParameters</span></span>
<span data-ttu-id="9e81c-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e81c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e81c-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e81c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e81c-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e81c-148">INPUTS</span></span>

### <span data-ttu-id="9e81c-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="9e81c-149">None</span></span>
<span data-ttu-id="9e81c-150">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9e81c-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e81c-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e81c-151">OUTPUTS</span></span>

### <span data-ttu-id="9e81c-152">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9e81c-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="9e81c-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e81c-153">NOTES</span></span>

## <span data-ttu-id="9e81c-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e81c-154">RELATED LINKS</span></span>

[<span data-ttu-id="9e81c-155">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9e81c-155">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="9e81c-156">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="9e81c-156">Get-AzureRmOperationalInsightsLinkTargets</span></span>](./Get-AzureRmOperationalInsightsLinkTargets.md)


