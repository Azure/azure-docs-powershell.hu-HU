---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.ADDomainServices/new-AzADDomainServiceReplicaSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
ms.openlocfilehash: ad11cbe364cd4d9cd8a667fd40a6a1d438f1aed4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935906"
---
# <span data-ttu-id="49377-101">New-AzADDomainServiceReplicaSet</span><span class="sxs-lookup"><span data-stu-id="49377-101">New-AzADDomainServiceReplicaSet</span></span>

## <span data-ttu-id="49377-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49377-102">SYNOPSIS</span></span>
<span data-ttu-id="49377-103">Memória-objektum létrehozása a Replikakészlethez</span><span class="sxs-lookup"><span data-stu-id="49377-103">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="49377-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49377-104">SYNTAX</span></span>

```
New-AzADDomainServiceReplicaSet [-Location <String>] [-SubnetId <String>] [<CommonParameters>]
```

## <span data-ttu-id="49377-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49377-105">DESCRIPTION</span></span>
<span data-ttu-id="49377-106">Memória-objektum létrehozása a Replikakészlethez</span><span class="sxs-lookup"><span data-stu-id="49377-106">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="49377-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49377-107">EXAMPLES</span></span>

### <span data-ttu-id="49377-108">1. példa: Replikakészlet létrehozása az AdDomainhoz</span><span class="sxs-lookup"><span data-stu-id="49377-108">Example 1: Create ReplicaSet for AdDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceReplicaSet -Location eastus -SubnetId /subscriptions/**********-****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/Microsoft.Network/virtualNetworks/yourinttest/subnets/default

DomainControllerIPAddress ExternalAccessIPAddress HealthLastEvaluated Location ServiceStatus SubnetId
------------------------- ----------------------- ------------------- -------- ------------- --------
                                                                      eastus                 /subscriptions/****
                                                                      ****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/M…
```

<span data-ttu-id="49377-109">Create ReplicaSet for AdDomain</span><span class="sxs-lookup"><span data-stu-id="49377-109">Create ReplicaSet for AdDomain</span></span>

## <span data-ttu-id="49377-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49377-110">PARAMETERS</span></span>

### <span data-ttu-id="49377-111">-Location</span><span class="sxs-lookup"><span data-stu-id="49377-111">-Location</span></span>
<span data-ttu-id="49377-112">Virtuális hálózati hely.</span><span class="sxs-lookup"><span data-stu-id="49377-112">Virtual network location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49377-113">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="49377-113">-SubnetId</span></span>
<span data-ttu-id="49377-114">Annak a virtuális hálózatnak a neve, amelybe a Tartományszolgáltatások telepítve lesznek.</span><span class="sxs-lookup"><span data-stu-id="49377-114">The name of the virtual network that Domain Services will be deployed on.</span></span>
<span data-ttu-id="49377-115">Annak az alhálózatnak az azonosítója, amelybe a Domain Services szolgáltatást telepíteni fogja.</span><span class="sxs-lookup"><span data-stu-id="49377-115">The id of the subnet that Domain Services will be deployed on.</span></span>
<span data-ttu-id="49377-116">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="49377-116">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49377-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49377-117">CommonParameters</span></span>
<span data-ttu-id="49377-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49377-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49377-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49377-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49377-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49377-120">INPUTS</span></span>

## <span data-ttu-id="49377-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49377-121">OUTPUTS</span></span>

### <span data-ttu-id="49377-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="49377-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span></span>

## <span data-ttu-id="49377-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49377-123">NOTES</span></span>

<span data-ttu-id="49377-124">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="49377-124">ALIASES</span></span>

## <span data-ttu-id="49377-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49377-125">RELATED LINKS</span></span>

