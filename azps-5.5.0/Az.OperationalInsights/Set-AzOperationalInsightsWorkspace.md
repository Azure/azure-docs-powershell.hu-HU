---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 5abfd1a02687eb2715ad924510176748e04e56cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206327"
---
# <span data-ttu-id="32188-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="32188-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="32188-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32188-102">SYNOPSIS</span></span>
<span data-ttu-id="32188-103">Frissíti a munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="32188-103">Updates a workspace.</span></span>

## <span data-ttu-id="32188-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="32188-104">SYNTAX</span></span>

### <span data-ttu-id="32188-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="32188-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="32188-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="32188-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="32188-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="32188-107">DESCRIPTION</span></span>
<span data-ttu-id="32188-108">A **Set-AzOperationalInsightsWorkspace** parancsmag módosítja a munkaterület konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="32188-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="32188-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="32188-109">EXAMPLES</span></span>

### <span data-ttu-id="32188-110">1. példa: Munkaterület módosítása név szerint</span><span class="sxs-lookup"><span data-stu-id="32188-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="32188-111">Ez a parancs módosítja a ContosoResourceGroup nevű erőforráscsoport MyWorkspace nevű munkaterületének termékváltozatát és címkéit.</span><span class="sxs-lookup"><span data-stu-id="32188-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="32188-112">2. példa: Munkaterület frissítése a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="32188-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="32188-113">Ez a parancs a Get-AzOperationalInsightsWorkspace-parancsmag segítségével begyűjte a MyWorkSpace nevű munkaterületet, majd átadja a **Set-AzOperationalInsightsWorkspace** parancsmagnak úgy, hogy a folyamatoperációs operátorral prémium szintűre állíthatja az SKU-t.</span><span class="sxs-lookup"><span data-stu-id="32188-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="32188-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32188-114">PARAMETERS</span></span>

### <span data-ttu-id="32188-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32188-115">-DefaultProfile</span></span>
<span data-ttu-id="32188-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="32188-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32188-117">-Name</span><span class="sxs-lookup"><span data-stu-id="32188-117">-Name</span></span>
<span data-ttu-id="32188-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32188-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="32188-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="32188-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="32188-120">A munkaterületen való hozzáféréshez szükséges hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="32188-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="32188-121">Az értéknek "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="32188-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="32188-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="32188-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="32188-123">A munkaterületi lekérdezés eléréséhez használható hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="32188-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="32188-124">Az értéknek "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="32188-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="32188-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32188-125">-ResourceGroupName</span></span>
<span data-ttu-id="32188-126">Az Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32188-126">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="32188-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="32188-127">-RetentionInDays</span></span>
<span data-ttu-id="32188-128">A munkaterület adatmegőrzési időszaka napokban.</span><span class="sxs-lookup"><span data-stu-id="32188-128">The workspace data retention in days.</span></span> <span data-ttu-id="32188-129">730 nap az összes többi skus maximálisan engedélyezett</span><span class="sxs-lookup"><span data-stu-id="32188-129">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="32188-130">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="32188-130">-Sku</span></span>
<span data-ttu-id="32188-131">A munkaterület szolgáltatási rétegét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="32188-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="32188-132">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="32188-132">Valid values are:</span></span> 
- <span data-ttu-id="32188-133">ingyenes</span><span class="sxs-lookup"><span data-stu-id="32188-133">free</span></span>
- <span data-ttu-id="32188-134">normál</span><span class="sxs-lookup"><span data-stu-id="32188-134">standard</span></span>
- <span data-ttu-id="32188-135">prémium</span><span class="sxs-lookup"><span data-stu-id="32188-135">premium</span></span>
- <span data-ttu-id="32188-136">pernode</span><span class="sxs-lookup"><span data-stu-id="32188-136">pernode</span></span>
- <span data-ttu-id="32188-137">különálló</span><span class="sxs-lookup"><span data-stu-id="32188-137">standalone</span></span>
- <span data-ttu-id="32188-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="32188-138">pergb2018</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone, pergb2018

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32188-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="32188-139">-Tag</span></span>
<span data-ttu-id="32188-140">A munkaterület erőforráscímkéi.</span><span class="sxs-lookup"><span data-stu-id="32188-140">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="32188-141">-Workspace</span><span class="sxs-lookup"><span data-stu-id="32188-141">-Workspace</span></span>
<span data-ttu-id="32188-142">Megadja a frissíthető munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="32188-142">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="32188-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32188-143">CommonParameters</span></span>
<span data-ttu-id="32188-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32188-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32188-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32188-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32188-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32188-146">INPUTS</span></span>

### <span data-ttu-id="32188-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="32188-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="32188-148">System.String</span><span class="sxs-lookup"><span data-stu-id="32188-148">System.String</span></span>

### <span data-ttu-id="32188-149">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="32188-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="32188-150">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="32188-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="32188-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32188-151">OUTPUTS</span></span>

### <span data-ttu-id="32188-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="32188-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="32188-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="32188-153">NOTES</span></span>

## <span data-ttu-id="32188-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32188-154">RELATED LINKS</span></span>

[<span data-ttu-id="32188-155">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="32188-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="32188-156">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="32188-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


