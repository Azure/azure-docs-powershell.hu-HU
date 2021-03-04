---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: db0ad78a942905846f764bb5d72a8ef3b209b6a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921513"
---
# <span data-ttu-id="bed87-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="bed87-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="bed87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bed87-102">SYNOPSIS</span></span>
<span data-ttu-id="bed87-103">Új alkalmazáselemzési erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="bed87-103">Create a new application insights resource</span></span>

## <span data-ttu-id="bed87-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bed87-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bed87-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bed87-105">DESCRIPTION</span></span>
<span data-ttu-id="bed87-106">Új alkalmazáselemzési erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="bed87-106">Create a new application insights resource</span></span>

## <span data-ttu-id="bed87-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bed87-107">EXAMPLES</span></span>

### <span data-ttu-id="bed87-108">1. példa: Új alkalmazásstatstatórata-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="bed87-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
PublicNetworkAccessForIngestion : Enabled
PublicNetworkAccessForQuery     : Enabled
PrivateLinkScopedResources      :
```

<span data-ttu-id="bed87-109">"java" típusú erőforráscsoport "teszt" nevű új alkalmazáselemzési erőforrás hozzáadása</span><span class="sxs-lookup"><span data-stu-id="bed87-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="bed87-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bed87-110">PARAMETERS</span></span>

### <span data-ttu-id="bed87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed87-111">-DefaultProfile</span></span>
<span data-ttu-id="bed87-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bed87-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bed87-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="bed87-113">-Kind</span></span>
<span data-ttu-id="bed87-114">Alkalmazás fajtája.</span><span class="sxs-lookup"><span data-stu-id="bed87-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed87-115">-Location</span><span class="sxs-lookup"><span data-stu-id="bed87-115">-Location</span></span>
<span data-ttu-id="bed87-116">Application Insights erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="bed87-116">Application Insights Resource Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed87-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bed87-117">-Name</span></span>
<span data-ttu-id="bed87-118">Application Insights erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="bed87-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="bed87-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="bed87-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="bed87-120">Az Application Insights-adatokhoz való hozzáférés hálózati hozzáférési típusa.</span><span class="sxs-lookup"><span data-stu-id="bed87-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="bed87-121">Az értéknek "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="bed87-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed87-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="bed87-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="bed87-123">Az Application Insights lekérdezés eléréséhez használható hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="bed87-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="bed87-124">Az értéknek "Engedélyezve" vagy "Letiltva" értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="bed87-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed87-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bed87-125">-ResourceGroupName</span></span>
<span data-ttu-id="bed87-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bed87-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="bed87-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="bed87-127">-RetentionInDays</span></span>
<span data-ttu-id="bed87-128">Az adatmegőrzés alapértelmezés szerint 90 nap.</span><span class="sxs-lookup"><span data-stu-id="bed87-128">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed87-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="bed87-129">-Tag</span></span>
<span data-ttu-id="bed87-130">Összetevőcímkék.</span><span class="sxs-lookup"><span data-stu-id="bed87-130">Component Tags.</span></span>

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

### <span data-ttu-id="bed87-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bed87-131">-Confirm</span></span>
<span data-ttu-id="bed87-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bed87-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bed87-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bed87-133">-WhatIf</span></span>
<span data-ttu-id="bed87-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bed87-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bed87-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bed87-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bed87-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed87-136">CommonParameters</span></span>
<span data-ttu-id="bed87-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bed87-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed87-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bed87-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed87-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bed87-139">INPUTS</span></span>

### <span data-ttu-id="bed87-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="bed87-140">None</span></span>

## <span data-ttu-id="bed87-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bed87-141">OUTPUTS</span></span>

### <span data-ttu-id="bed87-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="bed87-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="bed87-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bed87-143">NOTES</span></span>

## <span data-ttu-id="bed87-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bed87-144">RELATED LINKS</span></span>
