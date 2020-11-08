---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: 19347de88b1b43c41f8ce774630e92dfc3ad592c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012869"
---
# <span data-ttu-id="991d8-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="991d8-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="991d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="991d8-102">SYNOPSIS</span></span>
<span data-ttu-id="991d8-103">meghívás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="991d8-103">removes an invitation</span></span>

## <span data-ttu-id="991d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="991d8-104">SYNTAX</span></span>

### <span data-ttu-id="991d8-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="991d8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="991d8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="991d8-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="991d8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="991d8-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="991d8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="991d8-108">DESCRIPTION</span></span>
<span data-ttu-id="991d8-109">A **Remove-AzDataShareInvitation** parancsmag eltávolítja a DataShare meghívót.</span><span class="sxs-lookup"><span data-stu-id="991d8-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="991d8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="991d8-110">EXAMPLES</span></span>

### <span data-ttu-id="991d8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="991d8-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="991d8-112">Ez a parancs eltávolítja a ADSInvite nevű meghívót a megosztás AdsShare.</span><span class="sxs-lookup"><span data-stu-id="991d8-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="991d8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="991d8-113">PARAMETERS</span></span>

### <span data-ttu-id="991d8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="991d8-114">-AccountName</span></span>
<span data-ttu-id="991d8-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="991d8-115">Azure data share account name</span></span>

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

### <span data-ttu-id="991d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="991d8-116">-DefaultProfile</span></span>
<span data-ttu-id="991d8-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="991d8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="991d8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="991d8-118">-InputObject</span></span>
<span data-ttu-id="991d8-119">Azure Data Share meghívás objektum</span><span class="sxs-lookup"><span data-stu-id="991d8-119">Azure data share invitation object</span></span>


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

### <span data-ttu-id="991d8-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="991d8-120">-Name</span></span>
<span data-ttu-id="991d8-121">Azure Data Share meghívás neve</span><span class="sxs-lookup"><span data-stu-id="991d8-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="991d8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="991d8-122">-PassThru</span></span>
<span data-ttu-id="991d8-123">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="991d8-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="991d8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="991d8-124">-ResourceGroupName</span></span>
<span data-ttu-id="991d8-125">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="991d8-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="991d8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="991d8-126">-ResourceId</span></span>
<span data-ttu-id="991d8-127">Az Azure-adatmegosztási meghívás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="991d8-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="991d8-128">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="991d8-128">-ShareName</span></span>
<span data-ttu-id="991d8-129">Azure-adatmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="991d8-129">Azure data share name.</span></span>

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

### <span data-ttu-id="991d8-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="991d8-130">-Confirm</span></span>
<span data-ttu-id="991d8-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="991d8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="991d8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="991d8-132">-WhatIf</span></span>
<span data-ttu-id="991d8-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="991d8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="991d8-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="991d8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="991d8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="991d8-135">CommonParameters</span></span>
<span data-ttu-id="991d8-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="991d8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="991d8-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="991d8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="991d8-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="991d8-138">INPUTS</span></span>

### <span data-ttu-id="991d8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="991d8-139">System.String</span></span>

### <span data-ttu-id="991d8-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="991d8-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="991d8-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="991d8-141">OUTPUTS</span></span>

### <span data-ttu-id="991d8-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="991d8-142">System.Boolean</span></span>

## <span data-ttu-id="991d8-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="991d8-143">NOTES</span></span>

## <span data-ttu-id="991d8-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="991d8-144">RELATED LINKS</span></span>
