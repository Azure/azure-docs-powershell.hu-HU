---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 74651ea4a9a108db9cc3f666ad6f78f494fcd676
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928177"
---
# <span data-ttu-id="41a7e-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="41a7e-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="41a7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="41a7e-103">Adatmegosztási fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="41a7e-103">Removes a datashare account</span></span>

## <span data-ttu-id="41a7e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="41a7e-104">SYNTAX</span></span>

### <span data-ttu-id="41a7e-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41a7e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41a7e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41a7e-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41a7e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41a7e-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41a7e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="41a7e-108">DESCRIPTION</span></span>
<span data-ttu-id="41a7e-109">A **Remove-AzDataShareAccount** parancsmag eltávolítja az adatmegosztási fiókot.</span><span class="sxs-lookup"><span data-stu-id="41a7e-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="41a7e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="41a7e-110">EXAMPLES</span></span>

### <span data-ttu-id="41a7e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="41a7e-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="41a7e-112">Ez a parancs eltávolítja a WikiADS nevű adatmegosztási fiókot az ADS nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="41a7e-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="41a7e-113">Ez a parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="41a7e-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="41a7e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41a7e-114">PARAMETERS</span></span>

### <span data-ttu-id="41a7e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41a7e-115">-AsJob</span></span>
<span data-ttu-id="41a7e-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="41a7e-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="41a7e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41a7e-117">-DefaultProfile</span></span>
<span data-ttu-id="41a7e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41a7e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41a7e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="41a7e-119">-Force</span></span>
<span data-ttu-id="41a7e-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="41a7e-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="41a7e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41a7e-121">-InputObject</span></span>
<span data-ttu-id="41a7e-122">Az Azure Data Share Account objektum.</span><span class="sxs-lookup"><span data-stu-id="41a7e-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41a7e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="41a7e-123">-Name</span></span>
<span data-ttu-id="41a7e-124">Azure data share account name.</span><span class="sxs-lookup"><span data-stu-id="41a7e-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="41a7e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41a7e-125">-PassThru</span></span>
<span data-ttu-id="41a7e-126">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="41a7e-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="41a7e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41a7e-127">-ResourceGroupName</span></span>
<span data-ttu-id="41a7e-128">Az Azure-adat-megosztási fiók erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="41a7e-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="41a7e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41a7e-129">-ResourceId</span></span>
<span data-ttu-id="41a7e-130">Az Azure-adat-megosztási fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="41a7e-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="41a7e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41a7e-131">-Confirm</span></span>
<span data-ttu-id="41a7e-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="41a7e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41a7e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41a7e-133">-WhatIf</span></span>
<span data-ttu-id="41a7e-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="41a7e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41a7e-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41a7e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41a7e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a7e-136">CommonParameters</span></span>
<span data-ttu-id="41a7e-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41a7e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a7e-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41a7e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a7e-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41a7e-139">INPUTS</span></span>

### <span data-ttu-id="41a7e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="41a7e-140">System.String</span></span>

### <span data-ttu-id="41a7e-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="41a7e-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="41a7e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41a7e-142">OUTPUTS</span></span>

### <span data-ttu-id="41a7e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="41a7e-143">System.Boolean</span></span>

## <span data-ttu-id="41a7e-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="41a7e-144">NOTES</span></span>

## <span data-ttu-id="41a7e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41a7e-145">RELATED LINKS</span></span>
