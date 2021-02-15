---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143594"
---
# <span data-ttu-id="10694-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="10694-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="10694-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10694-102">SYNOPSIS</span></span>
<span data-ttu-id="10694-103">IoT-biztonsági megoldás</span><span class="sxs-lookup"><span data-stu-id="10694-103">Get IoT security solution</span></span>

## <span data-ttu-id="10694-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="10694-104">SYNTAX</span></span>

### <span data-ttu-id="10694-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10694-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10694-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="10694-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10694-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="10694-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10694-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="10694-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10694-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="10694-109">DESCRIPTION</span></span>
<span data-ttu-id="10694-110">A Get-AzIotSecuritySolution parancsmag egy vagy több iot biztonsági megoldást ad vissza.</span><span class="sxs-lookup"><span data-stu-id="10694-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="10694-111">Az IoT biztonsági megoldás biztonsági adatokat és eseményeket gyűjt az iot-eszközökről és az iOT-központban a veszélyforrások megelőzése és észlelése érdekében.</span><span class="sxs-lookup"><span data-stu-id="10694-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="10694-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="10694-112">EXAMPLES</span></span>

### <span data-ttu-id="10694-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="10694-113">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "centraluseuap"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="10694-114">A MySample megoldás lekérte a "MyResourceGroup" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="10694-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="10694-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="10694-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="10694-116">A MyResourceGroup erőforráscsoport összes biztonsági megoldásának lekérte</span><span class="sxs-lookup"><span data-stu-id="10694-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="10694-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10694-117">PARAMETERS</span></span>

### <span data-ttu-id="10694-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10694-118">-DefaultProfile</span></span>
<span data-ttu-id="10694-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10694-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10694-120">-Name</span><span class="sxs-lookup"><span data-stu-id="10694-120">-Name</span></span>
<span data-ttu-id="10694-121">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="10694-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10694-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10694-122">-ResourceGroupName</span></span>
<span data-ttu-id="10694-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="10694-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10694-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10694-124">-ResourceId</span></span>
<span data-ttu-id="10694-125">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="10694-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10694-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10694-126">CommonParameters</span></span>
<span data-ttu-id="10694-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10694-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10694-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10694-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10694-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10694-129">INPUTS</span></span>

### <span data-ttu-id="10694-130">System.String</span><span class="sxs-lookup"><span data-stu-id="10694-130">System.String</span></span>

## <span data-ttu-id="10694-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10694-131">OUTPUTS</span></span>

### <span data-ttu-id="10694-132">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="10694-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="10694-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="10694-133">NOTES</span></span>

## <span data-ttu-id="10694-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10694-134">RELATED LINKS</span></span>
