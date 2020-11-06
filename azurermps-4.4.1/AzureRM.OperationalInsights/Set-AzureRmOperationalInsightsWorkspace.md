---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: e24597d25fffdc1b516c5a18cf011f7222d288c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493393"
---
# <span data-ttu-id="25734-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="25734-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="25734-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25734-102">SYNOPSIS</span></span>
<span data-ttu-id="25734-103">Munkaterületet frissít.</span><span class="sxs-lookup"><span data-stu-id="25734-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25734-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25734-104">SYNTAX</span></span>

### <span data-ttu-id="25734-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25734-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25734-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="25734-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tags] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25734-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="25734-107">DESCRIPTION</span></span>
<span data-ttu-id="25734-108">A **set-AzureRmOperationalInsightsWorkspace** parancsmag a munkaterület konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="25734-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="25734-109">Példák</span><span class="sxs-lookup"><span data-stu-id="25734-109">EXAMPLES</span></span>

### <span data-ttu-id="25734-110">Példa 1: munkaterület módosítása név szerint</span><span class="sxs-lookup"><span data-stu-id="25734-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="25734-111">Ez a parancs módosítja a MyWorkspace nevű munkaterület SKU-és címkéket a ContosoResourceGroup nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="25734-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="25734-112">2. példa: munkaterület frissítése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="25734-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="25734-113">Ez a parancs a Get-AzureRmOperationalInsightsWorkspace parancsmagot használja a MyWorkSpace nevű munkaterület beolvasásához, majd átadja azt a **set-AzureRmOperationalInsightsWorkspace** parancsmagnak a pipeline operátorral az SKU prémium értékre való beállításához.</span><span class="sxs-lookup"><span data-stu-id="25734-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="25734-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25734-114">PARAMETERS</span></span>

### <span data-ttu-id="25734-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="25734-115">-Name</span></span>
<span data-ttu-id="25734-116">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25734-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="25734-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25734-117">-ResourceGroupName</span></span>
<span data-ttu-id="25734-118">Az Azure Resource Group nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="25734-118">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="25734-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="25734-119">-Sku</span></span>
<span data-ttu-id="25734-120">A munkaterület szolgáltatási rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25734-120">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="25734-121">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="25734-121">Valid values are:</span></span> 

- <span data-ttu-id="25734-122">ingyenes</span><span class="sxs-lookup"><span data-stu-id="25734-122">free</span></span>
- <span data-ttu-id="25734-123">Standard</span><span class="sxs-lookup"><span data-stu-id="25734-123">standard</span></span>
- <span data-ttu-id="25734-124">prémium verzió</span><span class="sxs-lookup"><span data-stu-id="25734-124">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: free, standard, premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25734-125">-Címkék</span><span class="sxs-lookup"><span data-stu-id="25734-125">-Tags</span></span>
<span data-ttu-id="25734-126">A munkaterület erőforrás-címkéit adja meg.</span><span class="sxs-lookup"><span data-stu-id="25734-126">Specifies the resource tags for the workspace.</span></span>

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

### <span data-ttu-id="25734-127">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="25734-127">-Workspace</span></span>
<span data-ttu-id="25734-128">A frissítendő munkaterületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="25734-128">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="25734-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25734-129">-DefaultProfile</span></span>
<span data-ttu-id="25734-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25734-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25734-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="25734-131">-RetentionInDays</span></span>
<span data-ttu-id="25734-132">Munkaterület-adatmegőrzés napokban.</span><span class="sxs-lookup"><span data-stu-id="25734-132">The workspace data retention in days.</span></span> <span data-ttu-id="25734-133">a 730 napok az összes többi SKU számára megengedett maximális érték.</span><span class="sxs-lookup"><span data-stu-id="25734-133">730 days is the maximum allowed for all other Skus.</span></span>

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

### <span data-ttu-id="25734-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25734-134">CommonParameters</span></span>
<span data-ttu-id="25734-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25734-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25734-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25734-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25734-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25734-137">INPUTS</span></span>

### <span data-ttu-id="25734-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="25734-138">PSWorkspace</span></span>
<span data-ttu-id="25734-139">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="25734-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="25734-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25734-140">OUTPUTS</span></span>

### <span data-ttu-id="25734-141">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="25734-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="25734-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25734-142">NOTES</span></span>

## <span data-ttu-id="25734-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25734-143">RELATED LINKS</span></span>

[<span data-ttu-id="25734-144">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="25734-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="25734-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="25734-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


