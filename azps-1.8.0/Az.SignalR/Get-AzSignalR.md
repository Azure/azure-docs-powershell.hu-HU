---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: be286c0a0006f1b8b054f32269bc06dc05bcf515
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669096"
---
# <span data-ttu-id="f3400-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="f3400-101">Get-AzSignalR</span></span>

## <span data-ttu-id="f3400-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3400-102">SYNOPSIS</span></span>
<span data-ttu-id="f3400-103">Egy erőforrás-csoportban vagy egy előfizetésben egy adott jelző szolgáltatás vagy az összes jelző szolgáltatás beszerzése</span><span class="sxs-lookup"><span data-stu-id="f3400-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="f3400-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3400-104">SYNTAX</span></span>

### <span data-ttu-id="f3400-105">ListSignalRServiceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3400-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3400-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3400-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3400-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3400-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3400-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3400-108">DESCRIPTION</span></span>
<span data-ttu-id="f3400-109">Egy erőforrás-csoportban vagy egy előfizetésben egy adott jelző szolgáltatás vagy az összes jelző szolgáltatás beszerzése</span><span class="sxs-lookup"><span data-stu-id="f3400-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="f3400-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f3400-110">EXAMPLES</span></span>

### <span data-ttu-id="f3400-111">Az előfizetésben szereplő összes szignáló szolgáltatás beszerzése</span><span class="sxs-lookup"><span data-stu-id="f3400-111">Get all SignalR services in the subscription</span></span>
```powershell
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="f3400-112">Az összes jelzési szolgáltatás beszerzése egy erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="f3400-112">Get all SignalR services in a resource group</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="f3400-113">Speciális jelfeldolgozó szolgáltatás beszerzése</span><span class="sxs-lookup"><span data-stu-id="f3400-113">Get a specific SignalR service</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="f3400-114">Az alapértelmezett erőforráscsoport kinyerése adott jelzéssel</span><span class="sxs-lookup"><span data-stu-id="f3400-114">Get a specific SignalR service from the default resource group</span></span>

```powershell
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="f3400-115">Az alapértelmezett erőforráscsoport beállítható `Set-AzDefault -ResourceGroupName myResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="f3400-115">The default resource group can be set by `Set-AzDefault -ResourceGroupName myResourceGroup`.</span></span>

## <span data-ttu-id="f3400-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3400-116">PARAMETERS</span></span>

### <span data-ttu-id="f3400-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3400-117">-DefaultProfile</span></span>
<span data-ttu-id="f3400-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3400-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3400-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3400-119">-Name</span></span>
<span data-ttu-id="f3400-120">A szignáló szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="f3400-120">SignalR service name.</span></span>

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

### <span data-ttu-id="f3400-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3400-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3400-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f3400-122">Resource group name.</span></span>

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

### <span data-ttu-id="f3400-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3400-123">-ResourceId</span></span>
<span data-ttu-id="f3400-124">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f3400-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="f3400-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3400-125">CommonParameters</span></span>
<span data-ttu-id="f3400-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3400-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3400-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3400-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3400-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3400-128">INPUTS</span></span>

### <span data-ttu-id="f3400-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f3400-129">System.String</span></span>

## <span data-ttu-id="f3400-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3400-130">OUTPUTS</span></span>

### <span data-ttu-id="f3400-131">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="f3400-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="f3400-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3400-132">NOTES</span></span>

## <span data-ttu-id="f3400-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3400-133">RELATED LINKS</span></span>
