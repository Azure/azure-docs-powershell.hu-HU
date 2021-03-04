---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: e7287cff34420c7885f5cddef95e4ca3b09e881f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920369"
---
# <span data-ttu-id="63554-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="63554-101">Get-AzSignalR</span></span>

## <span data-ttu-id="63554-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63554-102">SYNOPSIS</span></span>
<span data-ttu-id="63554-103">Egy erőforráscsoportban vagy előfizetésben egy adott SignalR-szolgáltatást vagy az összes SignalR-szolgáltatást le kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="63554-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="63554-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="63554-104">SYNTAX</span></span>

### <span data-ttu-id="63554-105">ListSignalRServiceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="63554-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63554-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="63554-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63554-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63554-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63554-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="63554-108">DESCRIPTION</span></span>
<span data-ttu-id="63554-109">Egy erőforráscsoportban vagy előfizetésben egy adott SignalR-szolgáltatást vagy az összes SignalR-szolgáltatást le kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="63554-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="63554-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="63554-110">EXAMPLES</span></span>

### <span data-ttu-id="63554-111">Az előfizetésben elérhető összes SignalR-szolgáltatás lekérte</span><span class="sxs-lookup"><span data-stu-id="63554-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="63554-112">Erőforráscsoport összes SignalR-szolgáltatásának lekérte</span><span class="sxs-lookup"><span data-stu-id="63554-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="63554-113">Adott SignalR-szolgáltatás átvitele</span><span class="sxs-lookup"><span data-stu-id="63554-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="63554-114">Adott SignalR-szolgáltatás lekérte az alapértelmezett erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="63554-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="63554-115">Az alapértelmezett erőforráscsoportot a \` Set-AzDefault -ResourceGroupName myResourceGroup állíthatja \` be.</span><span class="sxs-lookup"><span data-stu-id="63554-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="63554-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63554-116">PARAMETERS</span></span>

### <span data-ttu-id="63554-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63554-117">-DefaultProfile</span></span>
<span data-ttu-id="63554-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63554-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63554-119">-Name</span><span class="sxs-lookup"><span data-stu-id="63554-119">-Name</span></span>
<span data-ttu-id="63554-120">SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="63554-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63554-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63554-121">-ResourceGroupName</span></span>
<span data-ttu-id="63554-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="63554-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63554-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63554-123">-ResourceId</span></span>
<span data-ttu-id="63554-124">A SignalR szolgáltatáserőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="63554-124">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63554-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63554-125">CommonParameters</span></span>
<span data-ttu-id="63554-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63554-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63554-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63554-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63554-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63554-128">INPUTS</span></span>

### <span data-ttu-id="63554-129">System.String</span><span class="sxs-lookup"><span data-stu-id="63554-129">System.String</span></span>
## <span data-ttu-id="63554-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63554-130">OUTPUTS</span></span>

### <span data-ttu-id="63554-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="63554-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="63554-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="63554-132">NOTES</span></span>

## <span data-ttu-id="63554-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63554-133">RELATED LINKS</span></span>
