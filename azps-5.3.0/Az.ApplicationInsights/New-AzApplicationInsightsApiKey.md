---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2afb8ebfa1305e736a226f48022f4c56ded2d809
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381371"
---
# <span data-ttu-id="84e6f-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="84e6f-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="84e6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="84e6f-103">Alkalmazás-betekintések api-kulcsának létrehozása egy alkalmazásstatékony erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="84e6f-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="84e6f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="84e6f-104">SYNTAX</span></span>

### <span data-ttu-id="84e6f-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84e6f-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84e6f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84e6f-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84e6f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84e6f-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84e6f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="84e6f-108">DESCRIPTION</span></span>
<span data-ttu-id="84e6f-109">Alkalmazás-betekintések api-kulcsának létrehozása egy alkalmazásstatékony erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="84e6f-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="84e6f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="84e6f-110">EXAMPLES</span></span>

### <span data-ttu-id="84e6f-111">1. példa: Új Api-kulcs létrehozása egy alkalmazásstatstatóforráshoz</span><span class="sxs-lookup"><span data-stu-id="84e6f-111">Example 1 Create a new Api Key for an application insights resource</span></span>
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

<span data-ttu-id="84e6f-112">Az "readtelemetry", a "testGroup" erőforráscsoport "test" erőforráscsoportjának "WriteAnnotations" engedélyekkel rendelkező "testapiKey" engedélyekkel létrehozhatja az alkalmazásstatizálási api kulcsleírását.</span><span class="sxs-lookup"><span data-stu-id="84e6f-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="84e6f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84e6f-113">PARAMETERS</span></span>

### <span data-ttu-id="84e6f-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="84e6f-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="84e6f-115">Application Insights összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="84e6f-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="84e6f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e6f-116">-DefaultProfile</span></span>
<span data-ttu-id="84e6f-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84e6f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84e6f-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="84e6f-118">-Description</span></span>
<span data-ttu-id="84e6f-119">Leírás az API-kulcs azonosításához.</span><span class="sxs-lookup"><span data-stu-id="84e6f-119">Description to help identify this API key.</span></span>

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

### <span data-ttu-id="84e6f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="84e6f-120">-Name</span></span>
<span data-ttu-id="84e6f-121">Összetevő neve.</span><span class="sxs-lookup"><span data-stu-id="84e6f-121">Component Name.</span></span>

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

### <span data-ttu-id="84e6f-122">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="84e6f-122">-Permissions</span></span>
<span data-ttu-id="84e6f-123">Engedélyek, amelyek használatát az API-kulcs engedélyezi az alkalmazások számára.</span><span class="sxs-lookup"><span data-stu-id="84e6f-123">Permissions that API key allow apps to do.</span></span>

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

### <span data-ttu-id="84e6f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84e6f-124">-ResourceGroupName</span></span>
<span data-ttu-id="84e6f-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="84e6f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="84e6f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84e6f-126">-ResourceId</span></span>
<span data-ttu-id="84e6f-127">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="84e6f-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="84e6f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84e6f-128">-Confirm</span></span>
<span data-ttu-id="84e6f-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="84e6f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84e6f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84e6f-130">-WhatIf</span></span>
<span data-ttu-id="84e6f-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="84e6f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84e6f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="84e6f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84e6f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e6f-133">CommonParameters</span></span>
<span data-ttu-id="84e6f-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84e6f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e6f-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84e6f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e6f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84e6f-136">INPUTS</span></span>

### <span data-ttu-id="84e6f-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="84e6f-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="84e6f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="84e6f-138">System.String</span></span>

## <span data-ttu-id="84e6f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84e6f-139">OUTPUTS</span></span>

### <span data-ttu-id="84e6f-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="84e6f-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="84e6f-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="84e6f-141">NOTES</span></span>

## <span data-ttu-id="84e6f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84e6f-142">RELATED LINKS</span></span>
