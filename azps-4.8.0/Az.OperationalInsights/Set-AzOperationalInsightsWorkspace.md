---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 5abfd1a02687eb2715ad924510176748e04e56cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182942"
---
# <span data-ttu-id="de4f0-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="de4f0-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="de4f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de4f0-102">SYNOPSIS</span></span>
<span data-ttu-id="de4f0-103">Munkaterületet frissít.</span><span class="sxs-lookup"><span data-stu-id="de4f0-103">Updates a workspace.</span></span>

## <span data-ttu-id="de4f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de4f0-104">SYNTAX</span></span>

### <span data-ttu-id="de4f0-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de4f0-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="de4f0-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="de4f0-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="de4f0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="de4f0-107">DESCRIPTION</span></span>
<span data-ttu-id="de4f0-108">A **set-AzOperationalInsightsWorkspace** parancsmag a munkaterület konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="de4f0-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="de4f0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="de4f0-109">EXAMPLES</span></span>

### <span data-ttu-id="de4f0-110">Példa 1: munkaterület módosítása név szerint</span><span class="sxs-lookup"><span data-stu-id="de4f0-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="de4f0-111">Ez a parancs módosítja a MyWorkspace nevű munkaterület SKU-és címkéket a ContosoResourceGroup nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="de4f0-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="de4f0-112">2. példa: munkaterület frissítése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="de4f0-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="de4f0-113">Ez a parancs a Get-AzOperationalInsightsWorkspace parancsmagot használja a MyWorkSpace nevű munkaterület beolvasásához, majd átadja azt a **set-AzOperationalInsightsWorkspace** parancsmagnak a pipeline operátorral az SKU prémium értékre való beállításához.</span><span class="sxs-lookup"><span data-stu-id="de4f0-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="de4f0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de4f0-114">PARAMETERS</span></span>

### <span data-ttu-id="de4f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de4f0-115">-DefaultProfile</span></span>
<span data-ttu-id="de4f0-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="de4f0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de4f0-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de4f0-117">-Name</span></span>
<span data-ttu-id="de4f0-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de4f0-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="de4f0-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="de4f0-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="de4f0-120">A munkaterület lenyelésének eléréséhez szükséges hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="de4f0-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="de4f0-121">Az értéknek "engedélyezve" vagy "Letiltva" kell lennie.</span><span class="sxs-lookup"><span data-stu-id="de4f0-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="de4f0-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="de4f0-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="de4f0-123">A munkaterületi lekérdezések eléréséhez használt hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="de4f0-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="de4f0-124">Az értéknek "engedélyezve" vagy "Letiltva" kell lennie.</span><span class="sxs-lookup"><span data-stu-id="de4f0-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="de4f0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de4f0-125">-ResourceGroupName</span></span>
<span data-ttu-id="de4f0-126">Az Azure Resource Group nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="de4f0-126">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="de4f0-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="de4f0-127">-RetentionInDays</span></span>
<span data-ttu-id="de4f0-128">Munkaterület-adatmegőrzés napokban.</span><span class="sxs-lookup"><span data-stu-id="de4f0-128">The workspace data retention in days.</span></span> <span data-ttu-id="de4f0-129">a 730 napok az összes többi SKU számára megengedett maximális érték.</span><span class="sxs-lookup"><span data-stu-id="de4f0-129">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="de4f0-130">-SKU</span><span class="sxs-lookup"><span data-stu-id="de4f0-130">-Sku</span></span>
<span data-ttu-id="de4f0-131">A munkaterület szolgáltatási rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de4f0-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="de4f0-132">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="de4f0-132">Valid values are:</span></span> 
- <span data-ttu-id="de4f0-133">ingyenes</span><span class="sxs-lookup"><span data-stu-id="de4f0-133">free</span></span>
- <span data-ttu-id="de4f0-134">Standard</span><span class="sxs-lookup"><span data-stu-id="de4f0-134">standard</span></span>
- <span data-ttu-id="de4f0-135">prémium verzió</span><span class="sxs-lookup"><span data-stu-id="de4f0-135">premium</span></span>
- <span data-ttu-id="de4f0-136">pernode</span><span class="sxs-lookup"><span data-stu-id="de4f0-136">pernode</span></span>
- <span data-ttu-id="de4f0-137">különálló</span><span class="sxs-lookup"><span data-stu-id="de4f0-137">standalone</span></span>
- <span data-ttu-id="de4f0-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="de4f0-138">pergb2018</span></span>

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

### <span data-ttu-id="de4f0-139">-Címke</span><span class="sxs-lookup"><span data-stu-id="de4f0-139">-Tag</span></span>
<span data-ttu-id="de4f0-140">A munkaterület erőforrás-címkéi.</span><span class="sxs-lookup"><span data-stu-id="de4f0-140">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="de4f0-141">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="de4f0-141">-Workspace</span></span>
<span data-ttu-id="de4f0-142">A frissítendő munkaterületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="de4f0-142">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="de4f0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de4f0-143">CommonParameters</span></span>
<span data-ttu-id="de4f0-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de4f0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de4f0-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="de4f0-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de4f0-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de4f0-146">INPUTS</span></span>

### <span data-ttu-id="de4f0-147">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="de4f0-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="de4f0-148">System. String</span><span class="sxs-lookup"><span data-stu-id="de4f0-148">System.String</span></span>

### <span data-ttu-id="de4f0-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="de4f0-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="de4f0-150">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="de4f0-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="de4f0-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de4f0-151">OUTPUTS</span></span>

### <span data-ttu-id="de4f0-152">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="de4f0-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="de4f0-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de4f0-153">NOTES</span></span>

## <span data-ttu-id="de4f0-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de4f0-154">RELATED LINKS</span></span>

[<span data-ttu-id="de4f0-155">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="de4f0-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="de4f0-156">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="de4f0-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


