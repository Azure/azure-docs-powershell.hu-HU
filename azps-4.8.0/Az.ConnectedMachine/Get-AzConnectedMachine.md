---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: afb6a5bab6c2761095fb3ab69a2898aeeb53b45c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025715"
---
# <span data-ttu-id="b4095-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="b4095-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="b4095-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4095-102">SYNOPSIS</span></span>
<span data-ttu-id="b4095-103">Információt keres a modell nézetről vagy egy hibrid gép példány nézetéről.</span><span class="sxs-lookup"><span data-stu-id="b4095-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="b4095-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4095-104">SYNTAX</span></span>

### <span data-ttu-id="b4095-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4095-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b4095-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b4095-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b4095-107">Lista</span><span class="sxs-lookup"><span data-stu-id="b4095-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4095-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4095-108">DESCRIPTION</span></span>
<span data-ttu-id="b4095-109">Információt keres a modell nézetről vagy egy hibrid gép példány nézetéről.</span><span class="sxs-lookup"><span data-stu-id="b4095-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="b4095-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b4095-110">EXAMPLES</span></span>

### <span data-ttu-id="b4095-111">1. példa: az előfizetésben lévő összes csatlakoztatott gép listázása</span><span class="sxs-lookup"><span data-stu-id="b4095-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="b4095-112">Az előfizetésben lévő összes csatlakoztatott gép felsorolása.</span><span class="sxs-lookup"><span data-stu-id="b4095-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="b4095-113">Ha az előfizetés nincs megadva, az előfizetést az aktuális Azure PowerShell-környezetből fogja használni.</span><span class="sxs-lookup"><span data-stu-id="b4095-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="b4095-114">2. példa: az erőforráscsoport összes csatlakoztatott számítógépének listázása</span><span class="sxs-lookup"><span data-stu-id="b4095-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="b4095-115">Az erőforráscsoport összes csatlakoztatott számítógépének listázása</span><span class="sxs-lookup"><span data-stu-id="b4095-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="b4095-116">3. példa: csatlakoztatott gép beszerzése egy erőforrás-csoportban név szerint</span><span class="sxs-lookup"><span data-stu-id="b4095-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="b4095-117">Az erőforráscsoport csatlakoztatott számítógépének beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="b4095-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="b4095-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4095-118">PARAMETERS</span></span>

### <span data-ttu-id="b4095-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4095-119">-DefaultProfile</span></span>
<span data-ttu-id="b4095-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4095-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4095-121">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="b4095-121">-Expand</span></span>
<span data-ttu-id="b4095-122">A művelethez alkalmazni kívánt kifejezés kibontása.</span><span class="sxs-lookup"><span data-stu-id="b4095-122">The expand expression to apply on the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Support.InstanceViewTypes
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4095-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4095-123">-Name</span></span>
<span data-ttu-id="b4095-124">A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="b4095-124">The name of the hybrid machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4095-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4095-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4095-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b4095-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4095-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4095-127">-SubscriptionId</span></span>
<span data-ttu-id="b4095-128">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b4095-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b4095-129">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b4095-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4095-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4095-130">CommonParameters</span></span>
<span data-ttu-id="b4095-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4095-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4095-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b4095-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4095-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4095-133">INPUTS</span></span>

## <span data-ttu-id="b4095-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4095-134">OUTPUTS</span></span>

### <span data-ttu-id="b4095-135">Microsoft. Azure. PowerShell. parancsmagok. ConnectedMachine. modellek. Api20200802. IMachine</span><span class="sxs-lookup"><span data-stu-id="b4095-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="b4095-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4095-136">NOTES</span></span>

<span data-ttu-id="b4095-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b4095-137">ALIASES</span></span>

## <span data-ttu-id="b4095-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4095-138">RELATED LINKS</span></span>

