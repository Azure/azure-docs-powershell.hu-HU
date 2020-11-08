---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017822"
---
# <span data-ttu-id="e2473-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="e2473-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="e2473-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2473-102">SYNOPSIS</span></span>
<span data-ttu-id="e2473-103">Adatkészlet-megfeleltetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e2473-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="e2473-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2473-104">SYNTAX</span></span>

### <span data-ttu-id="e2473-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2473-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2473-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2473-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2473-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2473-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2473-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2473-108">DESCRIPTION</span></span>
<span data-ttu-id="e2473-109">A **Remove-AzDataShareDataSetMapping** parancsmag eltávolít egy adatkészlet-megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="e2473-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="e2473-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e2473-110">EXAMPLES</span></span>

### <span data-ttu-id="e2473-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e2473-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="e2473-112">Ez a parancs eltávolítja a DSM nevű adatkészletet a sharesubscription WikiAds.</span><span class="sxs-lookup"><span data-stu-id="e2473-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="e2473-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2473-113">PARAMETERS</span></span>

### <span data-ttu-id="e2473-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e2473-114">-AccountName</span></span>
<span data-ttu-id="e2473-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="e2473-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2473-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2473-116">-DefaultProfile</span></span>
<span data-ttu-id="e2473-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2473-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2473-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2473-118">-InputObject</span></span>
<span data-ttu-id="e2473-119">Az Azure Data Set megfeleltetési objektum</span><span class="sxs-lookup"><span data-stu-id="e2473-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2473-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2473-120">-Name</span></span>
<span data-ttu-id="e2473-121">Azure Data Set megfeleltetés neve</span><span class="sxs-lookup"><span data-stu-id="e2473-121">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2473-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2473-122">-PassThru</span></span>
<span data-ttu-id="e2473-123">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="e2473-123">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2473-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2473-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2473-125">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="e2473-125">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2473-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2473-126">-ResourceId</span></span>
<span data-ttu-id="e2473-127">Az Azure adathalmaz megfeleltetésének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e2473-127">The resource id of the azure data set mapping</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2473-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e2473-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="e2473-129">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="e2473-129">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2473-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2473-130">-Confirm</span></span>
<span data-ttu-id="e2473-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2473-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2473-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2473-132">-WhatIf</span></span>
<span data-ttu-id="e2473-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2473-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2473-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2473-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2473-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2473-135">CommonParameters</span></span>
<span data-ttu-id="e2473-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2473-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2473-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e2473-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2473-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2473-138">INPUTS</span></span>

### <span data-ttu-id="e2473-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e2473-139">System.String</span></span>

### <span data-ttu-id="e2473-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="e2473-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="e2473-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2473-141">OUTPUTS</span></span>

### <span data-ttu-id="e2473-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2473-142">System.Boolean</span></span>

## <span data-ttu-id="e2473-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2473-143">NOTES</span></span>

## <span data-ttu-id="e2473-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2473-144">RELATED LINKS</span></span>
