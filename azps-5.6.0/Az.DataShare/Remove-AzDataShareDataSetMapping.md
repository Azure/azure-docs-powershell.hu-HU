---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 8e3513621b94a7fc98a00b7eb443bef18d2a8141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937009"
---
# <span data-ttu-id="de233-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="de233-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="de233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de233-102">SYNOPSIS</span></span>
<span data-ttu-id="de233-103">Adatkészlet-megfeleltetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="de233-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="de233-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="de233-104">SYNTAX</span></span>

### <span data-ttu-id="de233-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de233-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de233-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de233-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de233-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de233-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de233-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="de233-108">DESCRIPTION</span></span>
<span data-ttu-id="de233-109">A **Remove-AzDataShareDataSetMapping** parancsmag eltávolítja az adatkészlet-megfeleltetéseket.</span><span class="sxs-lookup"><span data-stu-id="de233-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="de233-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="de233-110">EXAMPLES</span></span>

### <span data-ttu-id="de233-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="de233-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="de233-112">Ez a parancs eltávolítja a DSM nevű adatkészletet a sharesubscription WikiAdsből.</span><span class="sxs-lookup"><span data-stu-id="de233-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="de233-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de233-113">PARAMETERS</span></span>

### <span data-ttu-id="de233-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="de233-114">-AccountName</span></span>
<span data-ttu-id="de233-115">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="de233-115">Azure data share account name</span></span>

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

### <span data-ttu-id="de233-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de233-116">-DefaultProfile</span></span>
<span data-ttu-id="de233-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de233-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de233-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de233-118">-InputObject</span></span>
<span data-ttu-id="de233-119">Az Azure-adatkészlet megfeleltetési objektuma</span><span class="sxs-lookup"><span data-stu-id="de233-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="de233-120">-Name</span><span class="sxs-lookup"><span data-stu-id="de233-120">-Name</span></span>
<span data-ttu-id="de233-121">Azure-adatkészlet megfeleltetésének neve</span><span class="sxs-lookup"><span data-stu-id="de233-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="de233-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de233-122">-PassThru</span></span>
<span data-ttu-id="de233-123">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="de233-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="de233-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de233-124">-ResourceGroupName</span></span>
<span data-ttu-id="de233-125">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="de233-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="de233-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de233-126">-ResourceId</span></span>
<span data-ttu-id="de233-127">Az Azure-adatkészlet megfeleltetésének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="de233-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="de233-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="de233-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="de233-129">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="de233-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="de233-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de233-130">-Confirm</span></span>
<span data-ttu-id="de233-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="de233-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de233-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de233-132">-WhatIf</span></span>
<span data-ttu-id="de233-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="de233-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de233-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de233-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de233-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de233-135">CommonParameters</span></span>
<span data-ttu-id="de233-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de233-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de233-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de233-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de233-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de233-138">INPUTS</span></span>

### <span data-ttu-id="de233-139">System.String</span><span class="sxs-lookup"><span data-stu-id="de233-139">System.String</span></span>

### <span data-ttu-id="de233-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="de233-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="de233-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de233-141">OUTPUTS</span></span>

### <span data-ttu-id="de233-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de233-142">System.Boolean</span></span>

## <span data-ttu-id="de233-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="de233-143">NOTES</span></span>

## <span data-ttu-id="de233-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de233-144">RELATED LINKS</span></span>
