---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: a4584e4c0fc64920fbffb7e3d685a9be3ac04ad1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495319"
---
# <span data-ttu-id="23645-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="23645-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="23645-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23645-102">SYNOPSIS</span></span>
<span data-ttu-id="23645-103">Munkaterületet frissít.</span><span class="sxs-lookup"><span data-stu-id="23645-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23645-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23645-104">SYNTAX</span></span>

### <span data-ttu-id="23645-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23645-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23645-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="23645-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23645-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="23645-107">DESCRIPTION</span></span>
<span data-ttu-id="23645-108">A **set-AzureRmOperationalInsightsWorkspace** parancsmag a munkaterület konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="23645-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="23645-109">Példák</span><span class="sxs-lookup"><span data-stu-id="23645-109">EXAMPLES</span></span>

### <span data-ttu-id="23645-110">Példa 1: munkaterület módosítása név szerint</span><span class="sxs-lookup"><span data-stu-id="23645-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="23645-111">Ez a parancs módosítja a MyWorkspace nevű munkaterület SKU-és címkéket a ContosoResourceGroup nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="23645-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="23645-112">2. példa: munkaterület frissítése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="23645-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="23645-113">Ez a parancs a Get-AzureRmOperationalInsightsWorkspace parancsmagot használja a MyWorkSpace nevű munkaterület beolvasásához, majd átadja azt a **set-AzureRmOperationalInsightsWorkspace** parancsmagnak a pipeline operátorral az SKU prémium értékre való beállításához.</span><span class="sxs-lookup"><span data-stu-id="23645-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="23645-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23645-114">PARAMETERS</span></span>

### <span data-ttu-id="23645-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23645-115">-DefaultProfile</span></span>
<span data-ttu-id="23645-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="23645-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23645-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="23645-117">-Name</span></span>
<span data-ttu-id="23645-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="23645-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23645-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23645-119">-ResourceGroupName</span></span>
<span data-ttu-id="23645-120">Az Azure Resource Group nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="23645-120">Specifies the Azure resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23645-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="23645-121">-RetentionInDays</span></span>
<span data-ttu-id="23645-122">Munkaterület-adatmegőrzés napokban.</span><span class="sxs-lookup"><span data-stu-id="23645-122">The workspace data retention in days.</span></span> <span data-ttu-id="23645-123">a 730 napok az összes többi SKU számára megengedett maximális érték.</span><span class="sxs-lookup"><span data-stu-id="23645-123">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23645-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="23645-124">-Sku</span></span>
<span data-ttu-id="23645-125">A munkaterület szolgáltatási rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="23645-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="23645-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="23645-126">Valid values are:</span></span> 

- <span data-ttu-id="23645-127">ingyenes</span><span class="sxs-lookup"><span data-stu-id="23645-127">free</span></span>
- <span data-ttu-id="23645-128">Standard</span><span class="sxs-lookup"><span data-stu-id="23645-128">standard</span></span>
- <span data-ttu-id="23645-129">prémium verzió</span><span class="sxs-lookup"><span data-stu-id="23645-129">premium</span></span>

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

### <span data-ttu-id="23645-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="23645-130">-Tag</span></span>
<span data-ttu-id="23645-131">A munkaterület erőforrás-címkéi.</span><span class="sxs-lookup"><span data-stu-id="23645-131">The resource tags for the workspace.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23645-132">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="23645-132">-Workspace</span></span>
<span data-ttu-id="23645-133">A frissítendő munkaterületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="23645-133">Specifies the workspace to be updated.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23645-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23645-134">CommonParameters</span></span>
<span data-ttu-id="23645-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23645-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23645-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23645-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23645-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23645-137">INPUTS</span></span>

### <span data-ttu-id="23645-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="23645-138">PSWorkspace</span></span>
<span data-ttu-id="23645-139">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="23645-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="23645-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23645-140">OUTPUTS</span></span>

### <span data-ttu-id="23645-141">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="23645-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="23645-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23645-142">NOTES</span></span>

## <span data-ttu-id="23645-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23645-143">RELATED LINKS</span></span>

[<span data-ttu-id="23645-144">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="23645-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="23645-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="23645-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


