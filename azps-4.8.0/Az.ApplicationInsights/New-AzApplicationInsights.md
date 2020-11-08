---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 3faa93ced76fee1a1023011e1570c3819f6c2013
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017974"
---
# <span data-ttu-id="4d89c-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4d89c-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="4d89c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d89c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d89c-103">Új alkalmazás-betekintést tartalmazó erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="4d89c-103">Create a new application insights resource</span></span>

## <span data-ttu-id="4d89c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d89c-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d89c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d89c-105">DESCRIPTION</span></span>
<span data-ttu-id="4d89c-106">Új alkalmazás-betekintést tartalmazó erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="4d89c-106">Create a new application insights resource</span></span>

## <span data-ttu-id="4d89c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4d89c-107">EXAMPLES</span></span>

### <span data-ttu-id="4d89c-108">Példa 1 új alkalmazás-betekintést tartalmazó erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="4d89c-108">Example 1 Create a new application insights resource</span></span>
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

<span data-ttu-id="4d89c-109">A "teszt" nevű új alkalmazás hozzáadása a "testgroup" típusú "Java" típusú erőforrás-csoporthoz</span><span class="sxs-lookup"><span data-stu-id="4d89c-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="4d89c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d89c-110">PARAMETERS</span></span>

### <span data-ttu-id="4d89c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d89c-111">-DefaultProfile</span></span>
<span data-ttu-id="4d89c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d89c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d89c-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="4d89c-113">-Kind</span></span>
<span data-ttu-id="4d89c-114">Alkalmazás típusa.</span><span class="sxs-lookup"><span data-stu-id="4d89c-114">Application kind.</span></span>

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

### <span data-ttu-id="4d89c-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="4d89c-115">-Location</span></span>
<span data-ttu-id="4d89c-116">Az alkalmazás betekintést nyújt az erőforrás helyére.</span><span class="sxs-lookup"><span data-stu-id="4d89c-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="4d89c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d89c-117">-Name</span></span>
<span data-ttu-id="4d89c-118">Az alkalmazás betekintése az erőforrás nevével</span><span class="sxs-lookup"><span data-stu-id="4d89c-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="4d89c-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="4d89c-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="4d89c-120">A betekintési lenyelési adatok eléréséhez szükséges hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="4d89c-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="4d89c-121">Az értéknek "engedélyezve" vagy "Letiltva" kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4d89c-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="4d89c-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="4d89c-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="4d89c-123">Az alkalmazások keresési lekérdezéséhez hozzáférő hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="4d89c-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="4d89c-124">Az értéknek "engedélyezve" vagy "Letiltva" kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4d89c-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="4d89c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d89c-125">-ResourceGroupName</span></span>
<span data-ttu-id="4d89c-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="4d89c-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="4d89c-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4d89c-127">-RetentionInDays</span></span>
<span data-ttu-id="4d89c-128">Az 90 alapértelmezés szerint napokban őrzi meg.</span><span class="sxs-lookup"><span data-stu-id="4d89c-128">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="4d89c-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="4d89c-129">-Tag</span></span>
<span data-ttu-id="4d89c-130">Összetevő-címkék.</span><span class="sxs-lookup"><span data-stu-id="4d89c-130">Component Tags.</span></span>

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

### <span data-ttu-id="4d89c-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4d89c-131">-Confirm</span></span>
<span data-ttu-id="4d89c-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d89c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d89c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d89c-133">-WhatIf</span></span>
<span data-ttu-id="4d89c-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4d89c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d89c-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d89c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d89c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d89c-136">CommonParameters</span></span>
<span data-ttu-id="4d89c-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d89c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d89c-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4d89c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d89c-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d89c-139">INPUTS</span></span>

### <span data-ttu-id="4d89c-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="4d89c-140">None</span></span>

## <span data-ttu-id="4d89c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d89c-141">OUTPUTS</span></span>

### <span data-ttu-id="4d89c-142">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4d89c-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="4d89c-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d89c-143">NOTES</span></span>

## <span data-ttu-id="4d89c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d89c-144">RELATED LINKS</span></span>
