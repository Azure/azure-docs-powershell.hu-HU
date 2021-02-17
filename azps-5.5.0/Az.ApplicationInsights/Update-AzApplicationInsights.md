---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210231"
---
# <span data-ttu-id="8dfd1-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8dfd1-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="8dfd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dfd1-102">SYNOPSIS</span></span>
<span data-ttu-id="8dfd1-103">meglévő alkalmazásstatikátó-erőforrás frissítése</span><span class="sxs-lookup"><span data-stu-id="8dfd1-103">update an existing application insights resource</span></span>

## <span data-ttu-id="8dfd1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8dfd1-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8dfd1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8dfd1-105">DESCRIPTION</span></span>
<span data-ttu-id="8dfd1-106">meglévő alkalmazásstatikátó-erőforrás frissítése</span><span class="sxs-lookup"><span data-stu-id="8dfd1-106">update an existing application insights resource</span></span>

## <span data-ttu-id="8dfd1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8dfd1-107">EXAMPLES</span></span>

### <span data-ttu-id="8dfd1-108">1. példa az Alkalmazásstatikációk összetevő frissítésére</span><span class="sxs-lookup"><span data-stu-id="8dfd1-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="8dfd1-109">Update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span><span class="sxs-lookup"><span data-stu-id="8dfd1-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="8dfd1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dfd1-110">PARAMETERS</span></span>

### <span data-ttu-id="8dfd1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dfd1-111">-DefaultProfile</span></span>
<span data-ttu-id="8dfd1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dfd1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8dfd1-113">-Name</span></span>
<span data-ttu-id="8dfd1-114">Application Insights erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="8dfd1-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="8dfd1-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="8dfd1-116">Az Application Insights-adatokhoz való hozzáférés hálózati hozzáférési típusa.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="8dfd1-117">Az értéknek "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-117">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="8dfd1-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="8dfd1-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="8dfd1-119">Az Application Insights lekérdezés eléréséhez használható hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="8dfd1-120">Az értéknek "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-120">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="8dfd1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dfd1-121">-ResourceGroupName</span></span>
<span data-ttu-id="8dfd1-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="8dfd1-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8dfd1-123">-RetentionInDays</span></span>
<span data-ttu-id="8dfd1-124">Az adatmegőrzés alapértelmezés szerint 90 nap.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-124">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="8dfd1-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="8dfd1-125">-Tag</span></span>
<span data-ttu-id="8dfd1-126">Összetevőcímkék.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-126">Component Tags.</span></span>

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

### <span data-ttu-id="8dfd1-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dfd1-127">-Confirm</span></span>
<span data-ttu-id="8dfd1-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dfd1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dfd1-129">-WhatIf</span></span>
<span data-ttu-id="8dfd1-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dfd1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dfd1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dfd1-132">CommonParameters</span></span>
<span data-ttu-id="8dfd1-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dfd1-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8dfd1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dfd1-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8dfd1-135">INPUTS</span></span>

### <span data-ttu-id="8dfd1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8dfd1-136">System.String</span></span>

## <span data-ttu-id="8dfd1-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8dfd1-137">OUTPUTS</span></span>

### <span data-ttu-id="8dfd1-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8dfd1-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="8dfd1-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8dfd1-139">NOTES</span></span>

## <span data-ttu-id="8dfd1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8dfd1-140">RELATED LINKS</span></span>
