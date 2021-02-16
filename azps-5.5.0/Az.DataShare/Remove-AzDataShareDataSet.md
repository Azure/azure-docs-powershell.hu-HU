---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161810"
---
# <span data-ttu-id="e766e-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="e766e-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="e766e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e766e-102">SYNOPSIS</span></span>
<span data-ttu-id="e766e-103">Adatkészlet-megfeleltetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e766e-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="e766e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e766e-104">SYNTAX</span></span>

### <span data-ttu-id="e766e-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e766e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e766e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e766e-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e766e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e766e-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e766e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e766e-108">DESCRIPTION</span></span>
<span data-ttu-id="e766e-109">A **Remove-AzDataShareDataSet** parancsmag eltávolít egy adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="e766e-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="e766e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e766e-110">EXAMPLES</span></span>

### <span data-ttu-id="e766e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e766e-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="e766e-112">Ez a parancs eltávolítja a DS nevű adatkészletet a megosztási WikiAdsből.</span><span class="sxs-lookup"><span data-stu-id="e766e-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="e766e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e766e-113">PARAMETERS</span></span>

### <span data-ttu-id="e766e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e766e-114">-AccountName</span></span>
<span data-ttu-id="e766e-115">Azure data share account name.</span><span class="sxs-lookup"><span data-stu-id="e766e-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="e766e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e766e-116">-DefaultProfile</span></span>
<span data-ttu-id="e766e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e766e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e766e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e766e-118">-InputObject</span></span>
<span data-ttu-id="e766e-119">Az Azure-adatkészlet-objektum.</span><span class="sxs-lookup"><span data-stu-id="e766e-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e766e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e766e-120">-Name</span></span>
<span data-ttu-id="e766e-121">Azure-adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="e766e-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e766e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e766e-122">-PassThru</span></span>
<span data-ttu-id="e766e-123">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="e766e-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="e766e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e766e-124">-ResourceGroupName</span></span>
<span data-ttu-id="e766e-125">Az Azure-adat-megosztási fiók erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="e766e-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="e766e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e766e-126">-ResourceId</span></span>
<span data-ttu-id="e766e-127">Az Azure-adatkészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e766e-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="e766e-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e766e-128">-ShareName</span></span>
<span data-ttu-id="e766e-129">Azure-adatok megosztásának neve.</span><span class="sxs-lookup"><span data-stu-id="e766e-129">Azure data share name.</span></span>

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

### <span data-ttu-id="e766e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e766e-130">-Confirm</span></span>
<span data-ttu-id="e766e-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e766e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e766e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e766e-132">-WhatIf</span></span>
<span data-ttu-id="e766e-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e766e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e766e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e766e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e766e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e766e-135">CommonParameters</span></span>
<span data-ttu-id="e766e-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e766e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e766e-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e766e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e766e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e766e-138">INPUTS</span></span>

### <span data-ttu-id="e766e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e766e-139">System.String</span></span>

### <span data-ttu-id="e766e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="e766e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="e766e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e766e-141">OUTPUTS</span></span>

### <span data-ttu-id="e766e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e766e-142">System.Boolean</span></span>

## <span data-ttu-id="e766e-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e766e-143">NOTES</span></span>

## <span data-ttu-id="e766e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e766e-144">RELATED LINKS</span></span>
