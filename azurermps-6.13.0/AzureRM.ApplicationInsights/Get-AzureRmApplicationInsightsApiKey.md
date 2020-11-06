---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 86ed0a3fc6dfef3dcfc111ff6d3a75dc78335924
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498515"
---
# <span data-ttu-id="f1a53-101">Get-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="f1a53-101">Get-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="f1a53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1a53-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a53-103">Az alkalmazás-elemzések API-kulcsai a betekintéshez</span><span class="sxs-lookup"><span data-stu-id="f1a53-103">Get application insights api keys for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1a53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1a53-104">SYNTAX</span></span>

### <span data-ttu-id="f1a53-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1a53-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1a53-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1a53-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1a53-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1a53-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1a53-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1a53-108">DESCRIPTION</span></span>
<span data-ttu-id="f1a53-109">Az alkalmazás-elemzések API-kulcsai a betekintéshez</span><span class="sxs-lookup"><span data-stu-id="f1a53-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="f1a53-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f1a53-110">EXAMPLES</span></span>

### <span data-ttu-id="f1a53-111">Példa 1 API-kulcsok beolvasása egy alkalmazásbeli betekintéshez</span><span class="sxs-lookup"><span data-stu-id="f1a53-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="f1a53-112">Az "ellenőrzés" az "testGroup" erőforráscsoport erőforrás csoportjának "teszt" csoportja.</span><span class="sxs-lookup"><span data-stu-id="f1a53-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="f1a53-113">Példa 2 speciális API-kulcs beolvasása egy alkalmazásbeli betekintéshez</span><span class="sxs-lookup"><span data-stu-id="f1a53-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="f1a53-114">A "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" erőforrás "teszt" az erőforráscsoport "testGroup".</span><span class="sxs-lookup"><span data-stu-id="f1a53-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="f1a53-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1a53-115">PARAMETERS</span></span>

### <span data-ttu-id="f1a53-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="f1a53-116">-ApiKeyId</span></span>
<span data-ttu-id="f1a53-117">Az alkalmazás betekintési API-kulcs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f1a53-117">Application Insights Api Key Id.</span></span>

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

### <span data-ttu-id="f1a53-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f1a53-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="f1a53-119">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="f1a53-119">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="f1a53-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a53-120">-DefaultProfile</span></span>
<span data-ttu-id="f1a53-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1a53-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1a53-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1a53-122">-Name</span></span>
<span data-ttu-id="f1a53-123">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="f1a53-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="f1a53-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a53-124">-ResourceGroupName</span></span>
<span data-ttu-id="f1a53-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f1a53-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f1a53-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1a53-126">-ResourceId</span></span>
<span data-ttu-id="f1a53-127">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f1a53-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="f1a53-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a53-128">CommonParameters</span></span>
<span data-ttu-id="f1a53-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1a53-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a53-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1a53-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a53-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1a53-131">INPUTS</span></span>

### <span data-ttu-id="f1a53-132">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f1a53-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="f1a53-133">Paraméterek: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f1a53-133">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="f1a53-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f1a53-134">System.String</span></span>

## <span data-ttu-id="f1a53-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1a53-135">OUTPUTS</span></span>

### <span data-ttu-id="f1a53-136">Microsoft. Azure. Command. ApplicationInsights. models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="f1a53-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="f1a53-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1a53-137">NOTES</span></span>

## <span data-ttu-id="f1a53-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1a53-138">RELATED LINKS</span></span>
