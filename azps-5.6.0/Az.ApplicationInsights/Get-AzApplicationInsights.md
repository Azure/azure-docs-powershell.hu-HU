---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
ms.openlocfilehash: f208722a065399c12facce6907bbcad3b64d46e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925250"
---
# <span data-ttu-id="0b419-101">Get-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0b419-101">Get-AzApplicationInsights</span></span>

## <span data-ttu-id="0b419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b419-102">SYNOPSIS</span></span>
<span data-ttu-id="0b419-103">Alkalmazáselemzési források lekérte</span><span class="sxs-lookup"><span data-stu-id="0b419-103">Get application insights resources</span></span>

## <span data-ttu-id="0b419-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0b419-104">SYNTAX</span></span>

### <span data-ttu-id="0b419-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0b419-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b419-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b419-106">ComponentNameParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b419-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b419-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b419-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0b419-108">DESCRIPTION</span></span>
<span data-ttu-id="0b419-109">Alkalmazáselemzési erőforrások lekérte egy erőforráscsoportban vagy adott erőforrásban</span><span class="sxs-lookup"><span data-stu-id="0b419-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="0b419-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0b419-110">EXAMPLES</span></span>

### <span data-ttu-id="0b419-111">1. példa: Alkalmazásstatikátás-erőforrás lekérte</span><span class="sxs-lookup"><span data-stu-id="0b419-111">Example 1 Get application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test"

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

<span data-ttu-id="0b419-112">"Teszt" nevű alkalmazáselemzési erőforrás lekérte a "tesztcsoport" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="0b419-112">Get application insights resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="0b419-113">2. példa: Alkalmazáselemzési erőforrás lekérte az árazási terv adatait</span><span class="sxs-lookup"><span data-stu-id="0b419-113">Example 2 Get application insights resource with pricing plan information</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -IncludePricingPlan

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

<span data-ttu-id="0b419-114">Alkalmazáselemzési erőforrás lekérte, és a "teszt" nevű erőforrás árazási tervének adatait is beveszi a "tesztcsoport" erőforráscsoportba</span><span class="sxs-lookup"><span data-stu-id="0b419-114">Get application insights resource and include pricing plan information for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="0b419-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b419-115">PARAMETERS</span></span>

### <span data-ttu-id="0b419-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b419-116">-DefaultProfile</span></span>
<span data-ttu-id="0b419-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b419-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b419-118">-Full</span><span class="sxs-lookup"><span data-stu-id="0b419-118">-Full</span></span>
<span data-ttu-id="0b419-119">Ha meg van adva, az alkalmazás vissza fogja kapni az árazási tervet/napi díjcsomagot, valamint az alkalmazásstatikációk összetevő állapotát.</span><span class="sxs-lookup"><span data-stu-id="0b419-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ComponentNameParameterSet, ResourceIdParameterSet
Aliases: IncludeDailyCap, IncludeDailyCapStatus, IncludePricingPlan

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b419-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0b419-120">-Name</span></span>
<span data-ttu-id="0b419-121">Application Insights erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0b419-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="0b419-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b419-122">-ResourceGroupName</span></span>
<span data-ttu-id="0b419-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0b419-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="0b419-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b419-124">-ResourceId</span></span>
<span data-ttu-id="0b419-125">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0b419-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="0b419-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b419-126">CommonParameters</span></span>
<span data-ttu-id="0b419-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b419-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b419-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b419-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b419-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b419-129">INPUTS</span></span>

### <span data-ttu-id="0b419-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0b419-130">System.String</span></span>

## <span data-ttu-id="0b419-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b419-131">OUTPUTS</span></span>

### <span data-ttu-id="0b419-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0b419-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="0b419-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0b419-133">NOTES</span></span>

## <span data-ttu-id="0b419-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b419-134">RELATED LINKS</span></span>
