---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2afb8ebfa1305e736a226f48022f4c56ded2d809
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149507"
---
# <span data-ttu-id="40589-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="40589-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="40589-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40589-102">SYNOPSIS</span></span>
<span data-ttu-id="40589-103">Alkalmazás-betekintések api-kulcsának létrehozása egy alkalmazásstatékony erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="40589-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="40589-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="40589-104">SYNTAX</span></span>

### <span data-ttu-id="40589-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40589-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40589-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40589-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40589-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40589-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40589-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="40589-108">DESCRIPTION</span></span>
<span data-ttu-id="40589-109">Alkalmazás-betekintések api-kulcsának létrehozása egy alkalmazásstatékony erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="40589-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="40589-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="40589-110">EXAMPLES</span></span>

### <span data-ttu-id="40589-111">1. példa: Új Api-kulcs létrehozása egy alkalmazásstatékony erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="40589-111">Example 1 Create a new Api Key for an application insights resource</span></span>
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

<span data-ttu-id="40589-112">Az "testGroup" erőforráscsoport "testGroup" erőforráscsoportjának "ReadTelemetry", "WriteAnnotations" engedélyekkel rendelkező "testapiKey" típusú, "WriteAnnotations" engedélyekkel rendelkező alkalmazásstatizálási api kulcsleírását hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="40589-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="40589-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40589-113">PARAMETERS</span></span>

### <span data-ttu-id="40589-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="40589-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="40589-115">Application Insights összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="40589-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="40589-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40589-116">-DefaultProfile</span></span>
<span data-ttu-id="40589-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40589-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40589-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="40589-118">-Description</span></span>
<span data-ttu-id="40589-119">Leírás az API-kulcs azonosításához.</span><span class="sxs-lookup"><span data-stu-id="40589-119">Description to help identify this API key.</span></span>

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

### <span data-ttu-id="40589-120">-Name</span><span class="sxs-lookup"><span data-stu-id="40589-120">-Name</span></span>
<span data-ttu-id="40589-121">Összetevő neve.</span><span class="sxs-lookup"><span data-stu-id="40589-121">Component Name.</span></span>

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

### <span data-ttu-id="40589-122">-Engedélyek</span><span class="sxs-lookup"><span data-stu-id="40589-122">-Permissions</span></span>
<span data-ttu-id="40589-123">Engedélyek, amelyek használatát az API-kulcs engedélyezi az alkalmazások számára.</span><span class="sxs-lookup"><span data-stu-id="40589-123">Permissions that API key allow apps to do.</span></span>

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

### <span data-ttu-id="40589-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40589-124">-ResourceGroupName</span></span>
<span data-ttu-id="40589-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="40589-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="40589-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40589-126">-ResourceId</span></span>
<span data-ttu-id="40589-127">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="40589-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="40589-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40589-128">-Confirm</span></span>
<span data-ttu-id="40589-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="40589-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40589-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40589-130">-WhatIf</span></span>
<span data-ttu-id="40589-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="40589-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40589-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40589-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40589-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40589-133">CommonParameters</span></span>
<span data-ttu-id="40589-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40589-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40589-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40589-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40589-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40589-136">INPUTS</span></span>

### <span data-ttu-id="40589-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="40589-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="40589-138">System.String</span><span class="sxs-lookup"><span data-stu-id="40589-138">System.String</span></span>

## <span data-ttu-id="40589-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40589-139">OUTPUTS</span></span>

### <span data-ttu-id="40589-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="40589-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="40589-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="40589-141">NOTES</span></span>

## <span data-ttu-id="40589-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40589-142">RELATED LINKS</span></span>
