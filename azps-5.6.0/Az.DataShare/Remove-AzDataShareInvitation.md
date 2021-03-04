---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: 4736a1b6e8d0a6d34cf1874868596d4139ad5e67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941834"
---
# <span data-ttu-id="49b36-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="49b36-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="49b36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b36-102">SYNOPSIS</span></span>
<span data-ttu-id="49b36-103">eltávolít egy meghívót</span><span class="sxs-lookup"><span data-stu-id="49b36-103">removes an invitation</span></span>

## <span data-ttu-id="49b36-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49b36-104">SYNTAX</span></span>

### <span data-ttu-id="49b36-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49b36-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49b36-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49b36-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49b36-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49b36-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49b36-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49b36-108">DESCRIPTION</span></span>
<span data-ttu-id="49b36-109">A **Remove-AzDataShareInvitation** parancsmag eltávolítja az adatmegosztási meghívásokat.</span><span class="sxs-lookup"><span data-stu-id="49b36-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="49b36-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49b36-110">EXAMPLES</span></span>

### <span data-ttu-id="49b36-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="49b36-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="49b36-112">Ez a parancs eltávolítja az ADSInvite nevű meghívást a share AdsShare-ről.</span><span class="sxs-lookup"><span data-stu-id="49b36-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="49b36-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49b36-113">PARAMETERS</span></span>

### <span data-ttu-id="49b36-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="49b36-114">-AccountName</span></span>
<span data-ttu-id="49b36-115">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="49b36-115">Azure data share account name</span></span>

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

### <span data-ttu-id="49b36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b36-116">-DefaultProfile</span></span>
<span data-ttu-id="49b36-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49b36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49b36-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49b36-118">-InputObject</span></span>
<span data-ttu-id="49b36-119">Azure-adatok megosztására vonatkozó meghívási objektum</span><span class="sxs-lookup"><span data-stu-id="49b36-119">Azure data share invitation object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49b36-120">-Name</span><span class="sxs-lookup"><span data-stu-id="49b36-120">-Name</span></span>
<span data-ttu-id="49b36-121">Azure-adatok megosztására szóló meghívás neve</span><span class="sxs-lookup"><span data-stu-id="49b36-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="49b36-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49b36-122">-PassThru</span></span>
<span data-ttu-id="49b36-123">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="49b36-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="49b36-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b36-124">-ResourceGroupName</span></span>
<span data-ttu-id="49b36-125">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="49b36-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="49b36-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49b36-126">-ResourceId</span></span>
<span data-ttu-id="49b36-127">Az Azure-adatok megosztására szóló meghívó erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="49b36-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="49b36-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="49b36-128">-ShareName</span></span>
<span data-ttu-id="49b36-129">Azure-adatok megosztásának neve.</span><span class="sxs-lookup"><span data-stu-id="49b36-129">Azure data share name.</span></span>

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

### <span data-ttu-id="49b36-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49b36-130">-Confirm</span></span>
<span data-ttu-id="49b36-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="49b36-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49b36-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49b36-132">-WhatIf</span></span>
<span data-ttu-id="49b36-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="49b36-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49b36-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49b36-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49b36-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b36-135">CommonParameters</span></span>
<span data-ttu-id="49b36-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b36-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b36-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49b36-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b36-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49b36-138">INPUTS</span></span>

### <span data-ttu-id="49b36-139">System.String</span><span class="sxs-lookup"><span data-stu-id="49b36-139">System.String</span></span>

### <span data-ttu-id="49b36-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="49b36-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="49b36-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49b36-141">OUTPUTS</span></span>

### <span data-ttu-id="49b36-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49b36-142">System.Boolean</span></span>

## <span data-ttu-id="49b36-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49b36-143">NOTES</span></span>

## <span data-ttu-id="49b36-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49b36-144">RELATED LINKS</span></span>
