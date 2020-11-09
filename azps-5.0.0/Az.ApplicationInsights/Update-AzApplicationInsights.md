---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300860"
---
# <span data-ttu-id="6153c-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6153c-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="6153c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6153c-102">SYNOPSIS</span></span>
<span data-ttu-id="6153c-103">meglévő alkalmazás-áttekintési erőforrás frissítése</span><span class="sxs-lookup"><span data-stu-id="6153c-103">update an existing application insights resource</span></span>

## <span data-ttu-id="6153c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6153c-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6153c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6153c-105">DESCRIPTION</span></span>
<span data-ttu-id="6153c-106">meglévő alkalmazás-áttekintési erőforrás frissítése</span><span class="sxs-lookup"><span data-stu-id="6153c-106">update an existing application insights resource</span></span>

## <span data-ttu-id="6153c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6153c-107">EXAMPLES</span></span>

### <span data-ttu-id="6153c-108">Példa 1 a betekintési összetevő frissítése</span><span class="sxs-lookup"><span data-stu-id="6153c-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="6153c-109">a "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery "disabled" ("disabled") állapotának frissítése</span><span class="sxs-lookup"><span data-stu-id="6153c-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="6153c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6153c-110">PARAMETERS</span></span>

### <span data-ttu-id="6153c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6153c-111">-DefaultProfile</span></span>
<span data-ttu-id="6153c-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6153c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6153c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6153c-113">-Name</span></span>
<span data-ttu-id="6153c-114">Az alkalmazás betekintése az erőforrás nevével</span><span class="sxs-lookup"><span data-stu-id="6153c-114">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6153c-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="6153c-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="6153c-116">A betekintési lenyelési adatok eléréséhez szükséges hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="6153c-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="6153c-117">Az értéknek "engedélyezve" vagy "Letiltva" kell lennie.</span><span class="sxs-lookup"><span data-stu-id="6153c-117">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6153c-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="6153c-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="6153c-119">Az alkalmazások keresési lekérdezéséhez hozzáférő hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="6153c-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="6153c-120">Az értéknek "engedélyezve" vagy "Letiltva" kell lennie.</span><span class="sxs-lookup"><span data-stu-id="6153c-120">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6153c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6153c-121">-ResourceGroupName</span></span>
<span data-ttu-id="6153c-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="6153c-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6153c-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="6153c-123">-RetentionInDays</span></span>
<span data-ttu-id="6153c-124">Az 90 alapértelmezés szerint napokban őrzi meg.</span><span class="sxs-lookup"><span data-stu-id="6153c-124">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6153c-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="6153c-125">-Tag</span></span>
<span data-ttu-id="6153c-126">Összetevő-címkék.</span><span class="sxs-lookup"><span data-stu-id="6153c-126">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6153c-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6153c-127">-Confirm</span></span>
<span data-ttu-id="6153c-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6153c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6153c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6153c-129">-WhatIf</span></span>
<span data-ttu-id="6153c-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6153c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6153c-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6153c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6153c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6153c-132">CommonParameters</span></span>
<span data-ttu-id="6153c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6153c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6153c-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6153c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6153c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6153c-135">INPUTS</span></span>

### <span data-ttu-id="6153c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6153c-136">System.String</span></span>

## <span data-ttu-id="6153c-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6153c-137">OUTPUTS</span></span>

### <span data-ttu-id="6153c-138">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6153c-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="6153c-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6153c-139">NOTES</span></span>

## <span data-ttu-id="6153c-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6153c-140">RELATED LINKS</span></span>
