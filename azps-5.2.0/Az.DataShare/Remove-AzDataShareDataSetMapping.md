---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333053"
---
# <span data-ttu-id="3640a-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="3640a-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="3640a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3640a-102">SYNOPSIS</span></span>
<span data-ttu-id="3640a-103">Adatkészlet-megfeleltetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3640a-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="3640a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3640a-104">SYNTAX</span></span>

### <span data-ttu-id="3640a-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3640a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3640a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3640a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3640a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3640a-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3640a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3640a-108">DESCRIPTION</span></span>
<span data-ttu-id="3640a-109">A **Remove-AzDataShareDataSetMapping** parancsmag eltávolítja az adatkészlet-megfeleltetéseket.</span><span class="sxs-lookup"><span data-stu-id="3640a-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="3640a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3640a-110">EXAMPLES</span></span>

### <span data-ttu-id="3640a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="3640a-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="3640a-112">Ez a parancs eltávolítja a DSM nevű adatkészletet a sharesubscription WikiAdsből.</span><span class="sxs-lookup"><span data-stu-id="3640a-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="3640a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3640a-113">PARAMETERS</span></span>

### <span data-ttu-id="3640a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3640a-114">-AccountName</span></span>
<span data-ttu-id="3640a-115">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="3640a-115">Azure data share account name</span></span>

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

### <span data-ttu-id="3640a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3640a-116">-DefaultProfile</span></span>
<span data-ttu-id="3640a-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3640a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3640a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3640a-118">-InputObject</span></span>
<span data-ttu-id="3640a-119">Az Azure-adatkészlet megfeleltetési objektuma</span><span class="sxs-lookup"><span data-stu-id="3640a-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="3640a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3640a-120">-Name</span></span>
<span data-ttu-id="3640a-121">Azure-adatkészlet megfeleltetésének neve</span><span class="sxs-lookup"><span data-stu-id="3640a-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="3640a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3640a-122">-PassThru</span></span>
<span data-ttu-id="3640a-123">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="3640a-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="3640a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3640a-124">-ResourceGroupName</span></span>
<span data-ttu-id="3640a-125">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="3640a-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="3640a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3640a-126">-ResourceId</span></span>
<span data-ttu-id="3640a-127">Az Azure-adatkészlet megfeleltetésének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3640a-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="3640a-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3640a-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="3640a-129">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="3640a-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="3640a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3640a-130">-Confirm</span></span>
<span data-ttu-id="3640a-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3640a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3640a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3640a-132">-WhatIf</span></span>
<span data-ttu-id="3640a-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3640a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3640a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3640a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3640a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3640a-135">CommonParameters</span></span>
<span data-ttu-id="3640a-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3640a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3640a-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3640a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3640a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3640a-138">INPUTS</span></span>

### <span data-ttu-id="3640a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3640a-139">System.String</span></span>

### <span data-ttu-id="3640a-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="3640a-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="3640a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3640a-141">OUTPUTS</span></span>

### <span data-ttu-id="3640a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3640a-142">System.Boolean</span></span>

## <span data-ttu-id="3640a-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3640a-143">NOTES</span></span>

## <span data-ttu-id="3640a-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3640a-144">RELATED LINKS</span></span>
