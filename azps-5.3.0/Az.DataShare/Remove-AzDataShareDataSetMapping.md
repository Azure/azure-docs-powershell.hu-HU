---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377129"
---
# <span data-ttu-id="bdcf5-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="bdcf5-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="bdcf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdcf5-102">SYNOPSIS</span></span>
<span data-ttu-id="bdcf5-103">Adatkészlet-megfeleltetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bdcf5-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="bdcf5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bdcf5-104">SYNTAX</span></span>

### <span data-ttu-id="bdcf5-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bdcf5-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdcf5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdcf5-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdcf5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdcf5-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdcf5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bdcf5-108">DESCRIPTION</span></span>
<span data-ttu-id="bdcf5-109">A **Remove-AzDataShareDataSetMapping** parancsmag eltávolítja az adatkészlet-megfeleltetéseket.</span><span class="sxs-lookup"><span data-stu-id="bdcf5-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="bdcf5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bdcf5-110">EXAMPLES</span></span>

### <span data-ttu-id="bdcf5-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="bdcf5-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="bdcf5-112">Ez a parancs eltávolítja a DSM nevű adatkészletet a sharesubscription WikiAdsből.</span><span class="sxs-lookup"><span data-stu-id="bdcf5-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="bdcf5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdcf5-113">PARAMETERS</span></span>

### <span data-ttu-id="bdcf5-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bdcf5-114">-AccountName</span></span>
<span data-ttu-id="bdcf5-115">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="bdcf5-115">Azure data share account name</span></span>

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

### <span data-ttu-id="bdcf5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdcf5-116">-DefaultProfile</span></span>
<span data-ttu-id="bdcf5-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bdcf5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdcf5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdcf5-118">-InputObject</span></span>
<span data-ttu-id="bdcf5-119">Az Azure-adatkészlet megfeleltetési objektuma</span><span class="sxs-lookup"><span data-stu-id="bdcf5-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="bdcf5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bdcf5-120">-Name</span></span>
<span data-ttu-id="bdcf5-121">Azure data set mapping name</span><span class="sxs-lookup"><span data-stu-id="bdcf5-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="bdcf5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdcf5-122">-PassThru</span></span>
<span data-ttu-id="bdcf5-123">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="bdcf5-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="bdcf5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdcf5-124">-ResourceGroupName</span></span>
<span data-ttu-id="bdcf5-125">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="bdcf5-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="bdcf5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdcf5-126">-ResourceId</span></span>
<span data-ttu-id="bdcf5-127">Az Azure-adatkészlet megfeleltetésének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="bdcf5-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="bdcf5-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="bdcf5-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="bdcf5-129">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="bdcf5-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="bdcf5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdcf5-130">-Confirm</span></span>
<span data-ttu-id="bdcf5-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bdcf5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdcf5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdcf5-132">-WhatIf</span></span>
<span data-ttu-id="bdcf5-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bdcf5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdcf5-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bdcf5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdcf5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdcf5-135">CommonParameters</span></span>
<span data-ttu-id="bdcf5-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdcf5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdcf5-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdcf5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdcf5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdcf5-138">INPUTS</span></span>

### <span data-ttu-id="bdcf5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bdcf5-139">System.String</span></span>

### <span data-ttu-id="bdcf5-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="bdcf5-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="bdcf5-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdcf5-141">OUTPUTS</span></span>

### <span data-ttu-id="bdcf5-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bdcf5-142">System.Boolean</span></span>

## <span data-ttu-id="bdcf5-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bdcf5-143">NOTES</span></span>

## <span data-ttu-id="bdcf5-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdcf5-144">RELATED LINKS</span></span>
