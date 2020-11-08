---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183443"
---
# <span data-ttu-id="ee9e6-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="ee9e6-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="ee9e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee9e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ee9e6-103">ExpressRoute-áramköri engedély létrehozása vagy frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="ee9e6-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="ee9e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee9e6-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ee9e6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee9e6-105">DESCRIPTION</span></span>
<span data-ttu-id="ee9e6-106">ExpressRoute-áramköri engedély létrehozása vagy frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="ee9e6-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="ee9e6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ee9e6-107">EXAMPLES</span></span>

### <span data-ttu-id="ee9e6-108">Példa 1: autorization létrehozása</span><span class="sxs-lookup"><span data-stu-id="ee9e6-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="ee9e6-109">Ez a parancsmag a privát felhőben létrehozta az engedélyt. `azps-test-auth``azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="ee9e6-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="ee9e6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee9e6-110">PARAMETERS</span></span>

### <span data-ttu-id="ee9e6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee9e6-111">-AsJob</span></span>
<span data-ttu-id="ee9e6-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="ee9e6-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee9e6-113">-DefaultProfile</span></span>
<span data-ttu-id="ee9e6-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee9e6-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee9e6-115">-Name</span></span>
<span data-ttu-id="ee9e6-116">A ExpressRoute-áramkör engedélyezésének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="ee9e6-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9e6-117">-Várva</span><span class="sxs-lookup"><span data-stu-id="ee9e6-117">-NoWait</span></span>
<span data-ttu-id="ee9e6-118">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="ee9e6-118">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9e6-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="ee9e6-119">-PrivateCloudName</span></span>
<span data-ttu-id="ee9e6-120">A privát felhő neve.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-120">The name of the private cloud.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9e6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee9e6-121">-ResourceGroupName</span></span>
<span data-ttu-id="ee9e6-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-122">The name of the resource group.</span></span>
<span data-ttu-id="ee9e6-123">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9e6-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee9e6-124">-SubscriptionId</span></span>
<span data-ttu-id="ee9e6-125">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9e6-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee9e6-126">-Confirm</span></span>
<span data-ttu-id="ee9e6-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee9e6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee9e6-128">-WhatIf</span></span>
<span data-ttu-id="ee9e6-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee9e6-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee9e6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee9e6-131">CommonParameters</span></span>
<span data-ttu-id="ee9e6-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee9e6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee9e6-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ee9e6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee9e6-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee9e6-134">INPUTS</span></span>

## <span data-ttu-id="ee9e6-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee9e6-135">OUTPUTS</span></span>

### <span data-ttu-id="ee9e6-136">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="ee9e6-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="ee9e6-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee9e6-137">NOTES</span></span>

<span data-ttu-id="ee9e6-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ee9e6-138">ALIASES</span></span>

## <span data-ttu-id="ee9e6-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee9e6-139">RELATED LINKS</span></span>

