---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195178"
---
# <span data-ttu-id="25021-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="25021-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="25021-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25021-102">SYNOPSIS</span></span>
<span data-ttu-id="25021-103">A IoT biztonsági megoldásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="25021-103">Get IoT security solution</span></span>

## <span data-ttu-id="25021-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25021-104">SYNTAX</span></span>

### <span data-ttu-id="25021-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25021-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25021-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="25021-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25021-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="25021-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25021-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="25021-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25021-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="25021-109">DESCRIPTION</span></span>
<span data-ttu-id="25021-110">A Get-AzIotSecuritySolution parancsmag egy vagy több IOT biztonsági megoldást ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="25021-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="25021-111">A IoT biztonsági megoldás biztonsági adatokat és eseményeket gyűjt a IoT-eszközökről és a IoT hub-ról a fenyegetések megelőzése és észlelése érdekében.</span><span class="sxs-lookup"><span data-stu-id="25021-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="25021-112">Példák</span><span class="sxs-lookup"><span data-stu-id="25021-112">EXAMPLES</span></span>

### <span data-ttu-id="25021-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="25021-113">Example 1</span></span>
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

<span data-ttu-id="25021-114">A "MySample" megoldás beszerzése az erőforráscsoport "MyResourceGroup" csoportjában</span><span class="sxs-lookup"><span data-stu-id="25021-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="25021-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="25021-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="25021-116">Az összes biztonsági megoldás listája az erőforráscsoport "MyResourceGroup" csoportjában</span><span class="sxs-lookup"><span data-stu-id="25021-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="25021-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25021-117">PARAMETERS</span></span>

### <span data-ttu-id="25021-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25021-118">-DefaultProfile</span></span>
<span data-ttu-id="25021-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25021-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25021-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="25021-120">-Name</span></span>
<span data-ttu-id="25021-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="25021-121">Resource name.</span></span>

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

### <span data-ttu-id="25021-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25021-122">-ResourceGroupName</span></span>
<span data-ttu-id="25021-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="25021-123">Resource group name.</span></span>

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

### <span data-ttu-id="25021-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25021-124">-ResourceId</span></span>
<span data-ttu-id="25021-125">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="25021-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="25021-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25021-126">CommonParameters</span></span>
<span data-ttu-id="25021-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25021-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25021-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="25021-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25021-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25021-129">INPUTS</span></span>

### <span data-ttu-id="25021-130">System. String</span><span class="sxs-lookup"><span data-stu-id="25021-130">System.String</span></span>

## <span data-ttu-id="25021-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25021-131">OUTPUTS</span></span>

### <span data-ttu-id="25021-132">Microsoft. Azure. commands. Security. models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="25021-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="25021-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25021-133">NOTES</span></span>

## <span data-ttu-id="25021-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25021-134">RELATED LINKS</span></span>