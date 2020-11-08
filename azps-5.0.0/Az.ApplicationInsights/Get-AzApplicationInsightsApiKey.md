---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 802dabc8373e1f3a97c66b9a9a7a121383b68287
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186923"
---
# <span data-ttu-id="93b76-101">Get-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="93b76-101">Get-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="93b76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93b76-102">SYNOPSIS</span></span>
<span data-ttu-id="93b76-103">Az alkalmazás-elemzések API-kulcsai a betekintéshez</span><span class="sxs-lookup"><span data-stu-id="93b76-103">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="93b76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93b76-104">SYNTAX</span></span>

### <span data-ttu-id="93b76-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93b76-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93b76-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93b76-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93b76-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93b76-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93b76-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="93b76-108">DESCRIPTION</span></span>
<span data-ttu-id="93b76-109">Az alkalmazás-elemzések API-kulcsai a betekintéshez</span><span class="sxs-lookup"><span data-stu-id="93b76-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="93b76-110">Példák</span><span class="sxs-lookup"><span data-stu-id="93b76-110">EXAMPLES</span></span>

### <span data-ttu-id="93b76-111">Példa 1 API-kulcsok beolvasása egy alkalmazásbeli betekintéshez</span><span class="sxs-lookup"><span data-stu-id="93b76-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="93b76-112">Az "ellenőrzés" az "testGroup" erőforráscsoport erőforrás csoportjának "teszt" csoportja.</span><span class="sxs-lookup"><span data-stu-id="93b76-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="93b76-113">Példa 2 speciális API-kulcs beolvasása egy alkalmazásbeli betekintéshez</span><span class="sxs-lookup"><span data-stu-id="93b76-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="93b76-114">A "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" erőforrás "teszt" az erőforráscsoport "testGroup".</span><span class="sxs-lookup"><span data-stu-id="93b76-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="93b76-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93b76-115">PARAMETERS</span></span>

### <span data-ttu-id="93b76-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="93b76-116">-ApiKeyId</span></span>
<span data-ttu-id="93b76-117">Az alkalmazás betekintési API-kulcs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="93b76-117">Application Insights Api Key Id.</span></span>

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

### <span data-ttu-id="93b76-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="93b76-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="93b76-119">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="93b76-119">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="93b76-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93b76-120">-DefaultProfile</span></span>
<span data-ttu-id="93b76-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93b76-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93b76-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="93b76-122">-Name</span></span>
<span data-ttu-id="93b76-123">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="93b76-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="93b76-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93b76-124">-ResourceGroupName</span></span>
<span data-ttu-id="93b76-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="93b76-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="93b76-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93b76-126">-ResourceId</span></span>
<span data-ttu-id="93b76-127">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="93b76-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="93b76-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b76-128">CommonParameters</span></span>
<span data-ttu-id="93b76-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93b76-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b76-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93b76-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b76-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93b76-131">INPUTS</span></span>

### <span data-ttu-id="93b76-132">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="93b76-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="93b76-133">System. String</span><span class="sxs-lookup"><span data-stu-id="93b76-133">System.String</span></span>

## <span data-ttu-id="93b76-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93b76-134">OUTPUTS</span></span>

### <span data-ttu-id="93b76-135">Microsoft. Azure. Command. ApplicationInsights. models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="93b76-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="93b76-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93b76-136">NOTES</span></span>

## <span data-ttu-id="93b76-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93b76-137">RELATED LINKS</span></span>