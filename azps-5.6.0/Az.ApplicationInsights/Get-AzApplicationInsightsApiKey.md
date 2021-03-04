---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 96887bebdfddec0a5393ca41bc3b552119cffe81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925242"
---
# <span data-ttu-id="97f67-101">Get-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="97f67-101">Get-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="97f67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97f67-102">SYNOPSIS</span></span>
<span data-ttu-id="97f67-103">Alkalmazások betekintő api-kulcsának lekérte egy alkalmazásstatékony erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="97f67-103">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="97f67-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="97f67-104">SYNTAX</span></span>

### <span data-ttu-id="97f67-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97f67-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97f67-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97f67-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97f67-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97f67-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97f67-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="97f67-108">DESCRIPTION</span></span>
<span data-ttu-id="97f67-109">Alkalmazások betekintő api-kulcsának lekérte egy alkalmazásstatékony erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="97f67-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="97f67-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="97f67-110">EXAMPLES</span></span>

### <span data-ttu-id="97f67-111">1. példa: Api-kulcsok lekérte egy alkalmazáselemzési erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="97f67-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="97f67-112">A "testGroup" erőforráscsoportban alkalmazásstatékony api-kulcsokat kaphat az erőforrás "teszt" csoportjához.</span><span class="sxs-lookup"><span data-stu-id="97f67-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="97f67-113">2. példa: Adott API-kulcs lekérte egy alkalmazás-elemzési erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="97f67-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="97f67-114">A "testGroup" erőforráscsoport "teszt" erőforráscsoportjában a "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" azonosítójú konkrét alkalmazásstatéria api-kulcsot kaphat.</span><span class="sxs-lookup"><span data-stu-id="97f67-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="97f67-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97f67-115">PARAMETERS</span></span>

### <span data-ttu-id="97f67-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="97f67-116">-ApiKeyId</span></span>
<span data-ttu-id="97f67-117">Application Insights API kulcsazonosító.</span><span class="sxs-lookup"><span data-stu-id="97f67-117">Application Insights Api Key Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97f67-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="97f67-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="97f67-119">Application Insights összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="97f67-119">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="97f67-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f67-120">-DefaultProfile</span></span>
<span data-ttu-id="97f67-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97f67-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97f67-122">-Name</span><span class="sxs-lookup"><span data-stu-id="97f67-122">-Name</span></span>
<span data-ttu-id="97f67-123">Application Insights összetevő neve.</span><span class="sxs-lookup"><span data-stu-id="97f67-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="97f67-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97f67-124">-ResourceGroupName</span></span>
<span data-ttu-id="97f67-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="97f67-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="97f67-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97f67-126">-ResourceId</span></span>
<span data-ttu-id="97f67-127">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="97f67-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="97f67-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f67-128">CommonParameters</span></span>
<span data-ttu-id="97f67-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97f67-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f67-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97f67-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f67-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97f67-131">INPUTS</span></span>

### <span data-ttu-id="97f67-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="97f67-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="97f67-133">System.String</span><span class="sxs-lookup"><span data-stu-id="97f67-133">System.String</span></span>

## <span data-ttu-id="97f67-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97f67-134">OUTPUTS</span></span>

### <span data-ttu-id="97f67-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="97f67-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="97f67-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="97f67-136">NOTES</span></span>

## <span data-ttu-id="97f67-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97f67-137">RELATED LINKS</span></span>
