---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: e339becd21be14d3587252b88dd8069b266b2408
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847733"
---
# <span data-ttu-id="18c20-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="18c20-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="18c20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18c20-102">SYNOPSIS</span></span>
<span data-ttu-id="18c20-103">Munkaterületet frissít.</span><span class="sxs-lookup"><span data-stu-id="18c20-103">Updates a workspace.</span></span>

## <span data-ttu-id="18c20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18c20-104">SYNTAX</span></span>

### <span data-ttu-id="18c20-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18c20-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18c20-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="18c20-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18c20-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="18c20-107">DESCRIPTION</span></span>
<span data-ttu-id="18c20-108">A **set-AzOperationalInsightsWorkspace** parancsmag a munkaterület konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="18c20-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="18c20-109">Példák</span><span class="sxs-lookup"><span data-stu-id="18c20-109">EXAMPLES</span></span>

### <span data-ttu-id="18c20-110">Példa 1: munkaterület módosítása név szerint</span><span class="sxs-lookup"><span data-stu-id="18c20-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="18c20-111">Ez a parancs módosítja a MyWorkspace nevű munkaterület SKU-és címkéket a ContosoResourceGroup nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="18c20-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="18c20-112">2. példa: munkaterület frissítése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="18c20-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="18c20-113">Ez a parancs a Get-AzOperationalInsightsWorkspace parancsmagot használja a MyWorkSpace nevű munkaterület beolvasásához, majd átadja azt a **set-AzOperationalInsightsWorkspace** parancsmagnak a pipeline operátorral az SKU prémium értékre való beállításához.</span><span class="sxs-lookup"><span data-stu-id="18c20-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="18c20-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18c20-114">PARAMETERS</span></span>

### <span data-ttu-id="18c20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c20-115">-DefaultProfile</span></span>
<span data-ttu-id="18c20-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="18c20-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18c20-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18c20-117">-Name</span></span>
<span data-ttu-id="18c20-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18c20-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18c20-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18c20-119">-ResourceGroupName</span></span>
<span data-ttu-id="18c20-120">Az Azure Resource Group nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="18c20-120">Specifies the Azure resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18c20-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="18c20-121">-RetentionInDays</span></span>
<span data-ttu-id="18c20-122">Munkaterület-adatmegőrzés napokban.</span><span class="sxs-lookup"><span data-stu-id="18c20-122">The workspace data retention in days.</span></span> <span data-ttu-id="18c20-123">a 730 napok az összes többi SKU számára megengedett maximális érték.</span><span class="sxs-lookup"><span data-stu-id="18c20-123">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18c20-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="18c20-124">-Sku</span></span>
<span data-ttu-id="18c20-125">A munkaterület szolgáltatási rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18c20-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="18c20-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="18c20-126">Valid values are:</span></span> 
- <span data-ttu-id="18c20-127">ingyenes</span><span class="sxs-lookup"><span data-stu-id="18c20-127">free</span></span>
- <span data-ttu-id="18c20-128">Standard</span><span class="sxs-lookup"><span data-stu-id="18c20-128">standard</span></span>
- <span data-ttu-id="18c20-129">prémium verzió</span><span class="sxs-lookup"><span data-stu-id="18c20-129">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18c20-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="18c20-130">-Tag</span></span>
<span data-ttu-id="18c20-131">A munkaterület erőforrás-címkéi.</span><span class="sxs-lookup"><span data-stu-id="18c20-131">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18c20-132">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="18c20-132">-Workspace</span></span>
<span data-ttu-id="18c20-133">A frissítendő munkaterületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="18c20-133">Specifies the workspace to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18c20-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c20-134">CommonParameters</span></span>
<span data-ttu-id="18c20-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18c20-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c20-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18c20-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c20-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18c20-137">INPUTS</span></span>

### <span data-ttu-id="18c20-138">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="18c20-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="18c20-139">System. String</span><span class="sxs-lookup"><span data-stu-id="18c20-139">System.String</span></span>

### <span data-ttu-id="18c20-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="18c20-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="18c20-141">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="18c20-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="18c20-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18c20-142">OUTPUTS</span></span>

### <span data-ttu-id="18c20-143">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="18c20-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="18c20-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18c20-144">NOTES</span></span>

## <span data-ttu-id="18c20-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18c20-145">RELATED LINKS</span></span>

[<span data-ttu-id="18c20-146">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="18c20-146">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="18c20-147">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="18c20-147">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


