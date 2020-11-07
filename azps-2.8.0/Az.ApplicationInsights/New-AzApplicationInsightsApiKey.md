---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: c4f972971b52e6ff8e7bac4ebcb0850ef71846ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667902"
---
# <span data-ttu-id="1fffd-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="1fffd-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="1fffd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1fffd-102">SYNOPSIS</span></span>
<span data-ttu-id="1fffd-103">A betekintést használó erőforrásokhoz tartozó alkalmazás-ismertető API-kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="1fffd-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="1fffd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1fffd-104">SYNTAX</span></span>

### <span data-ttu-id="1fffd-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1fffd-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fffd-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fffd-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fffd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fffd-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fffd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1fffd-108">DESCRIPTION</span></span>
<span data-ttu-id="1fffd-109">Az alkalmazás-elemzések API-kulcsainak létrehozása az alkalmazásbeli betekintéshez</span><span class="sxs-lookup"><span data-stu-id="1fffd-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="1fffd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1fffd-110">EXAMPLES</span></span>

### <span data-ttu-id="1fffd-111">Példa 1 új API-kulcs létrehozása az alkalmazásbeli betekintések erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="1fffd-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="1fffd-112">Az alkalmazások API-testapiKey "ReadTelemetry", "WriteAnnotations" "" az erőforrás "teszt" erőforráscsoport "testGroup" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="1fffd-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="1fffd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1fffd-113">PARAMETERS</span></span>

### <span data-ttu-id="1fffd-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1fffd-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="1fffd-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="1fffd-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fffd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fffd-116">-DefaultProfile</span></span>
<span data-ttu-id="1fffd-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1fffd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fffd-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1fffd-118">-Description</span></span>
<span data-ttu-id="1fffd-119">Az API-kulcs meghatározását segítő Leírás</span><span class="sxs-lookup"><span data-stu-id="1fffd-119">Description to help identify this API key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fffd-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1fffd-120">-Name</span></span>
<span data-ttu-id="1fffd-121">Összetevő neve</span><span class="sxs-lookup"><span data-stu-id="1fffd-121">Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fffd-122">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="1fffd-122">-Permissions</span></span>
<span data-ttu-id="1fffd-123">Az API-kulcs engedélyezése az alkalmazások számára.</span><span class="sxs-lookup"><span data-stu-id="1fffd-123">Permissions that API key allow apps to do.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fffd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fffd-124">-ResourceGroupName</span></span>
<span data-ttu-id="1fffd-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1fffd-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fffd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fffd-126">-ResourceId</span></span>
<span data-ttu-id="1fffd-127">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1fffd-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fffd-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1fffd-128">-Confirm</span></span>
<span data-ttu-id="1fffd-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1fffd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fffd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fffd-130">-WhatIf</span></span>
<span data-ttu-id="1fffd-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1fffd-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fffd-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1fffd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fffd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fffd-133">CommonParameters</span></span>
<span data-ttu-id="1fffd-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1fffd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fffd-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fffd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fffd-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fffd-136">INPUTS</span></span>

### <span data-ttu-id="1fffd-137">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1fffd-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="1fffd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1fffd-138">System.String</span></span>

## <span data-ttu-id="1fffd-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fffd-139">OUTPUTS</span></span>

### <span data-ttu-id="1fffd-140">Microsoft. Azure. Command. ApplicationInsights. models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="1fffd-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="1fffd-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1fffd-141">NOTES</span></span>

## <span data-ttu-id="1fffd-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1fffd-142">RELATED LINKS</span></span>
