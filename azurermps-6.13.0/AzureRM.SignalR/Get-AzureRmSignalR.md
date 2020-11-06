---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
ms.openlocfilehash: 08e68a878267f706c280c8d461e8c904141cd06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497287"
---
# <span data-ttu-id="f28cb-101">Get-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="f28cb-101">Get-AzureRmSignalR</span></span>

## <span data-ttu-id="f28cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f28cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f28cb-103">Egy erőforrás-csoportban vagy egy előfizetésben egy adott jelző szolgáltatás vagy az összes jelző szolgáltatás beszerzése</span><span class="sxs-lookup"><span data-stu-id="f28cb-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f28cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f28cb-104">SYNTAX</span></span>

### <span data-ttu-id="f28cb-105">ListSignalRServiceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f28cb-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f28cb-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f28cb-106">ResourceGroupParameterSet</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f28cb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f28cb-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f28cb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f28cb-108">DESCRIPTION</span></span>
<span data-ttu-id="f28cb-109">Egy erőforrás-csoportban vagy egy előfizetésben egy adott jelző szolgáltatás vagy az összes jelző szolgáltatás beszerzése</span><span class="sxs-lookup"><span data-stu-id="f28cb-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="f28cb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f28cb-110">EXAMPLES</span></span>

### <span data-ttu-id="f28cb-111">Az előfizetésben szereplő összes szignáló szolgáltatás beszerzése</span><span class="sxs-lookup"><span data-stu-id="f28cb-111">Get all SignalR services in the subscription</span></span>
```powershell
PS C:\> Get-AzureRmSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="f28cb-112">Az összes jelzési szolgáltatás beszerzése egy erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="f28cb-112">Get all SignalR services in a resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="f28cb-113">Speciális jelfeldolgozó szolgáltatás beszerzése</span><span class="sxs-lookup"><span data-stu-id="f28cb-113">Get a specific SignalR service</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="f28cb-114">Az alapértelmezett erőforráscsoport kinyerése adott jelzéssel</span><span class="sxs-lookup"><span data-stu-id="f28cb-114">Get a specific SignalR service from the default resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="f28cb-115">Az alapértelmezett erőforráscsoport beállítható `Set-AzureRmDefault -ResourceGroupName myResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="f28cb-115">The default resource group can be set by `Set-AzureRmDefault -ResourceGroupName myResourceGroup`.</span></span>

## <span data-ttu-id="f28cb-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f28cb-116">PARAMETERS</span></span>

### <span data-ttu-id="f28cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f28cb-117">-DefaultProfile</span></span>
<span data-ttu-id="f28cb-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f28cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f28cb-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f28cb-119">-Name</span></span>
<span data-ttu-id="f28cb-120">A szignáló szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="f28cb-120">SignalR service name.</span></span>

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

### <span data-ttu-id="f28cb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f28cb-121">-ResourceGroupName</span></span>
<span data-ttu-id="f28cb-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f28cb-122">Resource group name.</span></span>

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

### <span data-ttu-id="f28cb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f28cb-123">-ResourceId</span></span>
<span data-ttu-id="f28cb-124">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f28cb-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="f28cb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f28cb-125">CommonParameters</span></span>
<span data-ttu-id="f28cb-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f28cb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f28cb-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f28cb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f28cb-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f28cb-128">INPUTS</span></span>

### <span data-ttu-id="f28cb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f28cb-129">System.String</span></span>
<span data-ttu-id="f28cb-130">Paraméterek: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f28cb-130">Parameters: ResourceId (ByValue)</span></span>

## <span data-ttu-id="f28cb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f28cb-131">OUTPUTS</span></span>

### <span data-ttu-id="f28cb-132">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="f28cb-132">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="f28cb-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f28cb-133">NOTES</span></span>

## <span data-ttu-id="f28cb-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f28cb-134">RELATED LINKS</span></span>
