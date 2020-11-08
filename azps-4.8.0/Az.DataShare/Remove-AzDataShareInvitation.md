---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: a94699bfa4b2637a0d0d51b8f52392bb02f51100
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017819"
---
# <span data-ttu-id="70370-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="70370-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="70370-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70370-102">SYNOPSIS</span></span>
<span data-ttu-id="70370-103">meghívás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="70370-103">removes an invitation</span></span>

## <span data-ttu-id="70370-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70370-104">SYNTAX</span></span>

### <span data-ttu-id="70370-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70370-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70370-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70370-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70370-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70370-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70370-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="70370-108">DESCRIPTION</span></span>
<span data-ttu-id="70370-109">A **Remove-AzDataShareInvitation** parancsmag eltávolítja a DataShare meghívót.</span><span class="sxs-lookup"><span data-stu-id="70370-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="70370-110">Példák</span><span class="sxs-lookup"><span data-stu-id="70370-110">EXAMPLES</span></span>

### <span data-ttu-id="70370-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="70370-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="70370-112">Ez a parancs eltávolítja a ADSInvite nevű meghívót a megosztás AdsShare.</span><span class="sxs-lookup"><span data-stu-id="70370-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="70370-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70370-113">PARAMETERS</span></span>

### <span data-ttu-id="70370-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="70370-114">-AccountName</span></span>
<span data-ttu-id="70370-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="70370-115">Azure data share account name</span></span>

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

### <span data-ttu-id="70370-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70370-116">-DefaultProfile</span></span>
<span data-ttu-id="70370-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70370-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70370-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70370-118">-InputObject</span></span>
<span data-ttu-id="70370-119">Azure Data Share meghívás objektum</span><span class="sxs-lookup"><span data-stu-id="70370-119">Azure data share invitation object</span></span>


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

### <span data-ttu-id="70370-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70370-120">-Name</span></span>
<span data-ttu-id="70370-121">Azure Data Share meghívás neve</span><span class="sxs-lookup"><span data-stu-id="70370-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="70370-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70370-122">-PassThru</span></span>
<span data-ttu-id="70370-123">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="70370-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="70370-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70370-124">-ResourceGroupName</span></span>
<span data-ttu-id="70370-125">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="70370-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="70370-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70370-126">-ResourceId</span></span>
<span data-ttu-id="70370-127">Az Azure-adatmegosztási meghívás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="70370-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="70370-128">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="70370-128">-ShareName</span></span>
<span data-ttu-id="70370-129">Azure-adatmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="70370-129">Azure data share name.</span></span>

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

### <span data-ttu-id="70370-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70370-130">-Confirm</span></span>
<span data-ttu-id="70370-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70370-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70370-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70370-132">-WhatIf</span></span>
<span data-ttu-id="70370-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70370-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70370-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70370-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70370-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70370-135">CommonParameters</span></span>
<span data-ttu-id="70370-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70370-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70370-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="70370-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70370-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70370-138">INPUTS</span></span>

### <span data-ttu-id="70370-139">System. String</span><span class="sxs-lookup"><span data-stu-id="70370-139">System.String</span></span>

### <span data-ttu-id="70370-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="70370-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="70370-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70370-141">OUTPUTS</span></span>

### <span data-ttu-id="70370-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70370-142">System.Boolean</span></span>

## <span data-ttu-id="70370-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70370-143">NOTES</span></span>

## <span data-ttu-id="70370-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70370-144">RELATED LINKS</span></span>
