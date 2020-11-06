---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsights.md
ms.openlocfilehash: 5e8fe7eeb2669bbde07f9ce3c6db868a6775e258
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496676"
---
# <span data-ttu-id="9f545-101">Get-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="9f545-101">Get-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="9f545-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f545-102">SYNOPSIS</span></span>
<span data-ttu-id="9f545-103">Az alkalmazások betekintési forrásai</span><span class="sxs-lookup"><span data-stu-id="9f545-103">Get application insights resources</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f545-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f545-104">SYNTAX</span></span>

### <span data-ttu-id="9f545-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f545-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f545-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f545-106">ComponentNameParameterSet</span></span>
```
Get-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f545-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f545-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f545-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f545-108">DESCRIPTION</span></span>
<span data-ttu-id="9f545-109">Az alkalmazások betekintése erőforrás-csoportokban vagy adott erőforrásokban</span><span class="sxs-lookup"><span data-stu-id="9f545-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="9f545-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9f545-110">EXAMPLES</span></span>

### <span data-ttu-id="9f545-111">Példa 1 a betekintést ismertető erőforrás beolvasása</span><span class="sxs-lookup"><span data-stu-id="9f545-111">Example 1 Get application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test"

Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
```

<span data-ttu-id="9f545-112">A "teszt" nevű erőforrás beolvasása a resoruce csoportban "testgroup"</span><span class="sxs-lookup"><span data-stu-id="9f545-112">Get application insights resource named "test" in resoruce group "testgroup"</span></span>

### <span data-ttu-id="9f545-113">2 példa a betekintési források beolvasása az árképzési terv adataival</span><span class="sxs-lookup"><span data-stu-id="9f545-113">Example 2 Get application insights resource with pricing plan information</span></span>
```
PS C:\> Get-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -IncludePricingPlan

Cap                            : 330
ResetTime                      : 0
StopSendNotificationWhenHitCap : True
CapExpirationTime              :
IsCapped                       : False
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
PricingPlan        : Basic
```

<span data-ttu-id="9f545-114">Betekintést kap az alkalmazásba, és belefoglalja a "teszt" nevű erőforrást a "testgroup" resoruce csoportjában</span><span class="sxs-lookup"><span data-stu-id="9f545-114">Get application insights resource and include pricing plan information for resource named "test" in resoruce group "testgroup"</span></span>

## <span data-ttu-id="9f545-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f545-115">PARAMETERS</span></span>

### <span data-ttu-id="9f545-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f545-116">-DefaultProfile</span></span>
<span data-ttu-id="9f545-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f545-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>


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

### <span data-ttu-id="9f545-118">-Full</span><span class="sxs-lookup"><span data-stu-id="9f545-118">-Full</span></span>
<span data-ttu-id="9f545-119">Ha meg van adva, a program visszaadja az árképzési terv/napi sapka és az alkalmazás állapotát.</span><span class="sxs-lookup"><span data-stu-id="9f545-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ComponentNameParameterSet, ResourceIdParameterSet
Aliases: IncludeDailyCap, IncludeDailyCapStatus, IncludePricingPlan

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f545-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9f545-120">-Name</span></span>
<span data-ttu-id="9f545-121">Az alkalmazás betekintése az erőforrás nevével</span><span class="sxs-lookup"><span data-stu-id="9f545-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="9f545-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f545-122">-ResourceGroupName</span></span>
<span data-ttu-id="9f545-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9f545-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="9f545-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f545-124">-ResourceId</span></span>
<span data-ttu-id="9f545-125">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9f545-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="9f545-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f545-126">CommonParameters</span></span>
<span data-ttu-id="9f545-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f545-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f545-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f545-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f545-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f545-129">INPUTS</span></span>

### <span data-ttu-id="9f545-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9f545-130">System.String</span></span>

## <span data-ttu-id="9f545-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f545-131">OUTPUTS</span></span>

### <span data-ttu-id="9f545-132">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9f545-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="9f545-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f545-133">NOTES</span></span>

## <span data-ttu-id="9f545-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f545-134">RELATED LINKS</span></span>

