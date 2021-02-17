---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165275"
---
# <span data-ttu-id="7c2ad-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="7c2ad-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="7c2ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="7c2ad-103">Adatkészlet-megfeleltetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7c2ad-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="7c2ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7c2ad-104">SYNTAX</span></span>

### <span data-ttu-id="7c2ad-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c2ad-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c2ad-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c2ad-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c2ad-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c2ad-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c2ad-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7c2ad-108">DESCRIPTION</span></span>
<span data-ttu-id="7c2ad-109">A **Remove-AzDataShareDataSetMapping** parancsmag eltávolítja az adatkészlet-megfeleltetéseket.</span><span class="sxs-lookup"><span data-stu-id="7c2ad-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="7c2ad-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7c2ad-110">EXAMPLES</span></span>

### <span data-ttu-id="7c2ad-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7c2ad-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="7c2ad-112">Ez a parancs eltávolítja a DSM nevű adatkészletet a sharesubscription WikiAdsből.</span><span class="sxs-lookup"><span data-stu-id="7c2ad-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="7c2ad-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c2ad-113">PARAMETERS</span></span>

### <span data-ttu-id="7c2ad-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7c2ad-114">-AccountName</span></span>
<span data-ttu-id="7c2ad-115">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="7c2ad-115">Azure data share account name</span></span>

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

### <span data-ttu-id="7c2ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c2ad-116">-DefaultProfile</span></span>
<span data-ttu-id="7c2ad-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c2ad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c2ad-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c2ad-118">-InputObject</span></span>
<span data-ttu-id="7c2ad-119">Az Azure-adatkészlet megfeleltetési objektuma</span><span class="sxs-lookup"><span data-stu-id="7c2ad-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="7c2ad-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7c2ad-120">-Name</span></span>
<span data-ttu-id="7c2ad-121">Azure-adatkészlet megfeleltetésének neve</span><span class="sxs-lookup"><span data-stu-id="7c2ad-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="7c2ad-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c2ad-122">-PassThru</span></span>
<span data-ttu-id="7c2ad-123">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="7c2ad-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="7c2ad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c2ad-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c2ad-125">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="7c2ad-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="7c2ad-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c2ad-126">-ResourceId</span></span>
<span data-ttu-id="7c2ad-127">Az Azure-adatkészlet megfeleltetésének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7c2ad-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="7c2ad-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="7c2ad-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="7c2ad-129">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="7c2ad-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="7c2ad-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c2ad-130">-Confirm</span></span>
<span data-ttu-id="7c2ad-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7c2ad-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c2ad-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c2ad-132">-WhatIf</span></span>
<span data-ttu-id="7c2ad-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7c2ad-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c2ad-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c2ad-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c2ad-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c2ad-135">CommonParameters</span></span>
<span data-ttu-id="7c2ad-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c2ad-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c2ad-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c2ad-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c2ad-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c2ad-138">INPUTS</span></span>

### <span data-ttu-id="7c2ad-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7c2ad-139">System.String</span></span>

### <span data-ttu-id="7c2ad-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="7c2ad-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="7c2ad-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c2ad-141">OUTPUTS</span></span>

### <span data-ttu-id="7c2ad-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c2ad-142">System.Boolean</span></span>

## <span data-ttu-id="7c2ad-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7c2ad-143">NOTES</span></span>

## <span data-ttu-id="7c2ad-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c2ad-144">RELATED LINKS</span></span>
