---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 550fb398dbd636ba9c43c66d31b78384610cf42b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014147"
---
# <span data-ttu-id="67b2d-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="67b2d-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="67b2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="67b2d-103">Új alkalmazás-betekintést tartalmazó erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="67b2d-103">Create a new application insights resource</span></span>

## <span data-ttu-id="67b2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67b2d-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67b2d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="67b2d-105">DESCRIPTION</span></span>
<span data-ttu-id="67b2d-106">Új alkalmazás-betekintést tartalmazó erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="67b2d-106">Create a new application insights resource</span></span>

## <span data-ttu-id="67b2d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="67b2d-107">EXAMPLES</span></span>

### <span data-ttu-id="67b2d-108">Példa 1 új alkalmazás-betekintést tartalmazó erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="67b2d-108">Example 1 Create a new application insights resource</span></span>
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
```

<span data-ttu-id="67b2d-109">Adjon hozzá egy új, "teszt" típusú erőforrást az "testgroup" és a "Java" nevű erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="67b2d-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="67b2d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67b2d-110">PARAMETERS</span></span>

### <span data-ttu-id="67b2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b2d-111">-DefaultProfile</span></span>
<span data-ttu-id="67b2d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67b2d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67b2d-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="67b2d-113">-Kind</span></span>
<span data-ttu-id="67b2d-114">Alkalmazás típusa.</span><span class="sxs-lookup"><span data-stu-id="67b2d-114">Application kind.</span></span>

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

### <span data-ttu-id="67b2d-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="67b2d-115">-Location</span></span>
<span data-ttu-id="67b2d-116">Az alkalmazás betekintést nyújt az erőforrás helyére.</span><span class="sxs-lookup"><span data-stu-id="67b2d-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="67b2d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="67b2d-117">-Name</span></span>
<span data-ttu-id="67b2d-118">Az alkalmazás betekintése az erőforrás nevével</span><span class="sxs-lookup"><span data-stu-id="67b2d-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="67b2d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67b2d-119">-ResourceGroupName</span></span>
<span data-ttu-id="67b2d-120">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="67b2d-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="67b2d-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="67b2d-121">-Tag</span></span>
<span data-ttu-id="67b2d-122">Összetevő-címkék.</span><span class="sxs-lookup"><span data-stu-id="67b2d-122">Component Tags.</span></span>

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

### <span data-ttu-id="67b2d-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="67b2d-123">-Confirm</span></span>
<span data-ttu-id="67b2d-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="67b2d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67b2d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67b2d-125">-WhatIf</span></span>
<span data-ttu-id="67b2d-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="67b2d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67b2d-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="67b2d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67b2d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b2d-128">CommonParameters</span></span>
<span data-ttu-id="67b2d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67b2d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b2d-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67b2d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b2d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67b2d-131">INPUTS</span></span>

### <span data-ttu-id="67b2d-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="67b2d-132">None</span></span>

## <span data-ttu-id="67b2d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67b2d-133">OUTPUTS</span></span>

### <span data-ttu-id="67b2d-134">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="67b2d-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="67b2d-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67b2d-135">NOTES</span></span>

## <span data-ttu-id="67b2d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67b2d-136">RELATED LINKS</span></span>
