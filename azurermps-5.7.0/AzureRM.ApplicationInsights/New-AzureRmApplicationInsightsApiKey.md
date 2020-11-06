---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 4c7f488e7a9ffca823128cccff18ba33b88dabfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499088"
---
# <span data-ttu-id="8ba6f-101">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="8ba6f-101">New-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="8ba6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ba6f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba6f-103">A betekintést használó erőforrásokhoz tartozó alkalmazás-ismertető API-kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="8ba6f-103">Create an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ba6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ba6f-104">SYNTAX</span></span>

### <span data-ttu-id="8ba6f-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ba6f-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ba6f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ba6f-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ba6f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ba6f-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ba6f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ba6f-108">DESCRIPTION</span></span>
<span data-ttu-id="8ba6f-109">Az alkalmazás-elemzések API-kulcsainak létrehozása az alkalmazásbeli betekintéshez</span><span class="sxs-lookup"><span data-stu-id="8ba6f-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="8ba6f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8ba6f-110">EXAMPLES</span></span>

### <span data-ttu-id="8ba6f-111">Példa 1 új API-kulcs létrehozása az alkalmazásbeli betekintések erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="8ba6f-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="8ba6f-112">Az alkalmazások API-testapiKey "ReadTelemetry", "WriteAnnotations" "" az erőforrás "teszt" erőforráscsoport "testGroup" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="8ba6f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ba6f-113">PARAMETERS</span></span>

### <span data-ttu-id="8ba6f-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8ba6f-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8ba6f-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba6f-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8ba6f-116">-Confirm</span></span>
<span data-ttu-id="8ba6f-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba6f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba6f-118">-DefaultProfile</span></span>
<span data-ttu-id="8ba6f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba6f-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="8ba6f-120">-Description</span></span>
<span data-ttu-id="8ba6f-121">Az API-kulcs meghatározását segítő Leírás</span><span class="sxs-lookup"><span data-stu-id="8ba6f-121">Description to help identify this API key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba6f-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8ba6f-122">-Name</span></span>
<span data-ttu-id="8ba6f-123">Összetevő neve</span><span class="sxs-lookup"><span data-stu-id="8ba6f-123">Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba6f-124">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="8ba6f-124">-Permissions</span></span>
<span data-ttu-id="8ba6f-125">Az API-kulcs engedélyezése az alkalmazások számára.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-125">Permissions that API key allow apps to do.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba6f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba6f-126">-ResourceGroupName</span></span>
<span data-ttu-id="8ba6f-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba6f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ba6f-128">-ResourceId</span></span>
<span data-ttu-id="8ba6f-129">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-129">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba6f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba6f-130">-WhatIf</span></span>
<span data-ttu-id="8ba6f-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ba6f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba6f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba6f-133">CommonParameters</span></span>
<span data-ttu-id="8ba6f-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ba6f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba6f-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ba6f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba6f-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ba6f-136">INPUTS</span></span>

### <span data-ttu-id="8ba6f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8ba6f-137">System.String</span></span>
<span data-ttu-id="8ba6f-138">System. string []</span><span class="sxs-lookup"><span data-stu-id="8ba6f-138">System.String[]</span></span>

## <span data-ttu-id="8ba6f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ba6f-139">OUTPUTS</span></span>

### <span data-ttu-id="8ba6f-140">Microsoft. Azure. Command. ApplicationInsights. models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="8ba6f-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="8ba6f-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ba6f-141">NOTES</span></span>

## <span data-ttu-id="8ba6f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ba6f-142">RELATED LINKS</span></span>

