---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: eb2b7f1e22ff3d2fccdff0d84a77f5c68ca8e70d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182812"
---
# <span data-ttu-id="27210-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="27210-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="27210-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27210-102">SYNOPSIS</span></span>
<span data-ttu-id="27210-103">megosztási előfizetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="27210-103">removes a share subscription</span></span>

## <span data-ttu-id="27210-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27210-104">SYNTAX</span></span>

### <span data-ttu-id="27210-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27210-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27210-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27210-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27210-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27210-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27210-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="27210-108">DESCRIPTION</span></span>
<span data-ttu-id="27210-109">A **Remove-AzDataShareSubscription** parancsmag eltávolít egy megosztási előfizetést</span><span class="sxs-lookup"><span data-stu-id="27210-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="27210-110">Példák</span><span class="sxs-lookup"><span data-stu-id="27210-110">EXAMPLES</span></span>

### <span data-ttu-id="27210-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="27210-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="27210-112">Ez a parancs eltávolítja a AdsShareSubscription nevű sharesubscription a fiók WikiAds.</span><span class="sxs-lookup"><span data-stu-id="27210-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="27210-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27210-113">PARAMETERS</span></span>

### <span data-ttu-id="27210-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="27210-114">-AccountName</span></span>
<span data-ttu-id="27210-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="27210-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="27210-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27210-116">-AsJob</span></span>
<span data-ttu-id="27210-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="27210-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="27210-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27210-118">-DefaultProfile</span></span>
<span data-ttu-id="27210-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27210-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27210-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27210-120">-InputObject</span></span>
<span data-ttu-id="27210-121">Azure Data Share-előfizetés objektum</span><span class="sxs-lookup"><span data-stu-id="27210-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27210-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27210-122">-Name</span></span>
<span data-ttu-id="27210-123">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="27210-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="27210-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27210-124">-PassThru</span></span>
<span data-ttu-id="27210-125">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="27210-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="27210-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27210-126">-ResourceGroupName</span></span>
<span data-ttu-id="27210-127">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="27210-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="27210-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27210-128">-ResourceId</span></span>
<span data-ttu-id="27210-129">Az Azure Data Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="27210-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="27210-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27210-130">-Confirm</span></span>
<span data-ttu-id="27210-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27210-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27210-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27210-132">-WhatIf</span></span>
<span data-ttu-id="27210-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27210-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27210-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27210-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27210-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27210-135">CommonParameters</span></span>
<span data-ttu-id="27210-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27210-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27210-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="27210-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27210-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27210-138">INPUTS</span></span>

### <span data-ttu-id="27210-139">System. String</span><span class="sxs-lookup"><span data-stu-id="27210-139">System.String</span></span>

### <span data-ttu-id="27210-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="27210-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="27210-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27210-141">OUTPUTS</span></span>

### <span data-ttu-id="27210-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27210-142">System.Boolean</span></span>

## <span data-ttu-id="27210-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27210-143">NOTES</span></span>

## <span data-ttu-id="27210-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27210-144">RELATED LINKS</span></span>
