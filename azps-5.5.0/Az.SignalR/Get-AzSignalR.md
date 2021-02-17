---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: f739c5fa018a4d4f4ebf553c76dbacd35ee315c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156275"
---
# <span data-ttu-id="3d13a-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="3d13a-101">Get-AzSignalR</span></span>

## <span data-ttu-id="3d13a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d13a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d13a-103">Egy erőforráscsoportban vagy előfizetésben egy adott SignalR-szolgáltatást vagy az összes SignalR-szolgáltatást le kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="3d13a-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="3d13a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3d13a-104">SYNTAX</span></span>

### <span data-ttu-id="3d13a-105">ListSignalRServiceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3d13a-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d13a-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d13a-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d13a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d13a-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d13a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3d13a-108">DESCRIPTION</span></span>
<span data-ttu-id="3d13a-109">Egy erőforráscsoportban vagy előfizetésben egy adott SignalR-szolgáltatást vagy az összes SignalR-szolgáltatást le kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="3d13a-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="3d13a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3d13a-110">EXAMPLES</span></span>

### <span data-ttu-id="3d13a-111">Az előfizetésben elérhető összes SignalR-szolgáltatás lekérte</span><span class="sxs-lookup"><span data-stu-id="3d13a-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="3d13a-112">Erőforráscsoport összes SignalR-szolgáltatásának lekérte</span><span class="sxs-lookup"><span data-stu-id="3d13a-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="3d13a-113">Adott SignalR-szolgáltatás átvitele</span><span class="sxs-lookup"><span data-stu-id="3d13a-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="3d13a-114">Adott SignalR-szolgáltatás lekérte az alapértelmezett erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="3d13a-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="3d13a-115">Az alapértelmezett erőforráscsoportot a \` Set-AzDefault -ResourceGroupName myResourceGroup állíthatja \` be.</span><span class="sxs-lookup"><span data-stu-id="3d13a-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="3d13a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d13a-116">PARAMETERS</span></span>

### <span data-ttu-id="3d13a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d13a-117">-DefaultProfile</span></span>
<span data-ttu-id="3d13a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d13a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d13a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3d13a-119">-Name</span></span>
<span data-ttu-id="3d13a-120">SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="3d13a-120">SignalR service name.</span></span>

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

### <span data-ttu-id="3d13a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d13a-121">-ResourceGroupName</span></span>
<span data-ttu-id="3d13a-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3d13a-122">Resource group name.</span></span>

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

### <span data-ttu-id="3d13a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d13a-123">-ResourceId</span></span>
<span data-ttu-id="3d13a-124">A SignalR szolgáltatás erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="3d13a-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="3d13a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d13a-125">CommonParameters</span></span>
<span data-ttu-id="3d13a-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d13a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d13a-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d13a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d13a-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d13a-128">INPUTS</span></span>

### <span data-ttu-id="3d13a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3d13a-129">System.String</span></span>
## <span data-ttu-id="3d13a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d13a-130">OUTPUTS</span></span>

### <span data-ttu-id="3d13a-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="3d13a-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="3d13a-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3d13a-132">NOTES</span></span>

## <span data-ttu-id="3d13a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d13a-133">RELATED LINKS</span></span>
