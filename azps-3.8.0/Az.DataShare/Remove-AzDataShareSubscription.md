---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: 12298f5c61981cb34572a104d39a279f7024adf2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012866"
---
# <span data-ttu-id="03374-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="03374-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="03374-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03374-102">SYNOPSIS</span></span>
<span data-ttu-id="03374-103">megosztási előfizetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="03374-103">removes a share subscription</span></span>

## <span data-ttu-id="03374-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03374-104">SYNTAX</span></span>

### <span data-ttu-id="03374-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03374-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03374-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03374-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03374-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03374-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03374-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="03374-108">DESCRIPTION</span></span>
<span data-ttu-id="03374-109">A **Remove-AzDataShareSubscription** parancsmag eltávolít egy megosztási előfizetést</span><span class="sxs-lookup"><span data-stu-id="03374-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="03374-110">Példák</span><span class="sxs-lookup"><span data-stu-id="03374-110">EXAMPLES</span></span>

### <span data-ttu-id="03374-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="03374-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="03374-112">Ez a parancs eltávolítja a AdsShareSubscription nevű sharesubscription a fiók WikiAds.</span><span class="sxs-lookup"><span data-stu-id="03374-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="03374-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03374-113">PARAMETERS</span></span>

### <span data-ttu-id="03374-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="03374-114">-AccountName</span></span>
<span data-ttu-id="03374-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="03374-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="03374-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03374-116">-AsJob</span></span>
<span data-ttu-id="03374-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="03374-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="03374-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03374-118">-DefaultProfile</span></span>
<span data-ttu-id="03374-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03374-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03374-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03374-120">-InputObject</span></span>
<span data-ttu-id="03374-121">Azure Data Share-előfizetés objektum</span><span class="sxs-lookup"><span data-stu-id="03374-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="03374-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="03374-122">-Name</span></span>
<span data-ttu-id="03374-123">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="03374-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="03374-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03374-124">-PassThru</span></span>
<span data-ttu-id="03374-125">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="03374-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="03374-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03374-126">-ResourceGroupName</span></span>
<span data-ttu-id="03374-127">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="03374-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="03374-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03374-128">-ResourceId</span></span>
<span data-ttu-id="03374-129">Az Azure Data Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="03374-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="03374-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="03374-130">-Confirm</span></span>
<span data-ttu-id="03374-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03374-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03374-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03374-132">-WhatIf</span></span>
<span data-ttu-id="03374-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="03374-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03374-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03374-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03374-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03374-135">CommonParameters</span></span>
<span data-ttu-id="03374-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03374-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03374-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03374-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03374-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03374-138">INPUTS</span></span>

### <span data-ttu-id="03374-139">System. String</span><span class="sxs-lookup"><span data-stu-id="03374-139">System.String</span></span>

### <span data-ttu-id="03374-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="03374-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="03374-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03374-141">OUTPUTS</span></span>

### <span data-ttu-id="03374-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03374-142">System.Boolean</span></span>

## <span data-ttu-id="03374-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03374-143">NOTES</span></span>

## <span data-ttu-id="03374-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03374-144">RELATED LINKS</span></span>
