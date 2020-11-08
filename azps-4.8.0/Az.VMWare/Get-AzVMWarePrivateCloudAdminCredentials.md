---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025026"
---
# <span data-ttu-id="e0cc6-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="e0cc6-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="e0cc6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="e0cc6-103">A személyes felhőhöz tartozó rendszergazdai hitelesítő adatok listája</span><span class="sxs-lookup"><span data-stu-id="e0cc6-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="e0cc6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0cc6-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e0cc6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0cc6-105">DESCRIPTION</span></span>
<span data-ttu-id="e0cc6-106">A személyes felhőhöz tartozó rendszergazdai hitelesítő adatok listája</span><span class="sxs-lookup"><span data-stu-id="e0cc6-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="e0cc6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e0cc6-107">EXAMPLES</span></span>

### <span data-ttu-id="e0cc6-108">Példa 1: titkos Felhőbeli rendszergazdai hitelesítő adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="e0cc6-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="e0cc6-109">Rendszergazdai hitelesítő adatok beszerzése Private Cloud-ról</span><span class="sxs-lookup"><span data-stu-id="e0cc6-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="e0cc6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0cc6-110">PARAMETERS</span></span>

### <span data-ttu-id="e0cc6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0cc6-111">-DefaultProfile</span></span>
<span data-ttu-id="e0cc6-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0cc6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0cc6-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="e0cc6-113">-PrivateCloudName</span></span>
<span data-ttu-id="e0cc6-114">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="e0cc6-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="e0cc6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0cc6-115">-ResourceGroupName</span></span>
<span data-ttu-id="e0cc6-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0cc6-116">The name of the resource group.</span></span>
<span data-ttu-id="e0cc6-117">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="e0cc6-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e0cc6-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0cc6-118">-SubscriptionId</span></span>
<span data-ttu-id="e0cc6-119">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e0cc6-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e0cc6-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0cc6-120">-Confirm</span></span>
<span data-ttu-id="e0cc6-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0cc6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0cc6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0cc6-122">-WhatIf</span></span>
<span data-ttu-id="e0cc6-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0cc6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0cc6-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0cc6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0cc6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0cc6-125">CommonParameters</span></span>
<span data-ttu-id="e0cc6-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0cc6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0cc6-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0cc6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0cc6-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0cc6-128">INPUTS</span></span>

## <span data-ttu-id="e0cc6-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0cc6-129">OUTPUTS</span></span>

### <span data-ttu-id="e0cc6-130">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. Api20200320. IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="e0cc6-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="e0cc6-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0cc6-131">NOTES</span></span>

<span data-ttu-id="e0cc6-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e0cc6-132">ALIASES</span></span>

## <span data-ttu-id="e0cc6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0cc6-133">RELATED LINKS</span></span>

