---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183437"
---
# <span data-ttu-id="14547-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="14547-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="14547-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14547-102">SYNOPSIS</span></span>
<span data-ttu-id="14547-103">Privát felhő létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="14547-103">Create or update a private cloud</span></span>

## <span data-ttu-id="14547-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14547-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="14547-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14547-105">DESCRIPTION</span></span>
<span data-ttu-id="14547-106">Privát felhő létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="14547-106">Create or update a private cloud</span></span>

## <span data-ttu-id="14547-107">Példák</span><span class="sxs-lookup"><span data-stu-id="14547-107">EXAMPLES</span></span>

### <span data-ttu-id="14547-108">Példa 1: privát felhő létrehozása</span><span class="sxs-lookup"><span data-stu-id="14547-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="14547-109">Privát felhő létrehozása</span><span class="sxs-lookup"><span data-stu-id="14547-109">Create private cloud</span></span>

## <span data-ttu-id="14547-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14547-110">PARAMETERS</span></span>

### <span data-ttu-id="14547-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14547-111">-AsJob</span></span>
<span data-ttu-id="14547-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="14547-112">Run the command as a job</span></span>

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

### <span data-ttu-id="14547-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14547-113">-DefaultProfile</span></span>
<span data-ttu-id="14547-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14547-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14547-115">-Internet</span><span class="sxs-lookup"><span data-stu-id="14547-115">-Internet</span></span>
<span data-ttu-id="14547-116">Az internethez való csatlakozás engedélyezve van vagy le van tiltva</span><span class="sxs-lookup"><span data-stu-id="14547-116">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14547-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="14547-117">-Location</span></span>
<span data-ttu-id="14547-118">Erőforrás-hely</span><span class="sxs-lookup"><span data-stu-id="14547-118">Resource location</span></span>

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

### <span data-ttu-id="14547-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="14547-119">-ManagementClusterSize</span></span>
<span data-ttu-id="14547-120">A szektorcsoport mérete</span><span class="sxs-lookup"><span data-stu-id="14547-120">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14547-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14547-121">-Name</span></span>
<span data-ttu-id="14547-122">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="14547-122">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14547-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="14547-123">-NetworkBlock</span></span>
<span data-ttu-id="14547-124">A címek blokkjának egyedinek kell lennie az előfizetése VNet, valamint a helyszíni.</span><span class="sxs-lookup"><span data-stu-id="14547-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="14547-125">Ellenőrizze, hogy a CIDR formátuma megfelel-e (A. B. C. D/X), ahol A, B, C, D 0 és 255 között van, az X pedig 0 és 22 között van</span><span class="sxs-lookup"><span data-stu-id="14547-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="14547-126">-Várva</span><span class="sxs-lookup"><span data-stu-id="14547-126">-NoWait</span></span>
<span data-ttu-id="14547-127">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="14547-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="14547-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="14547-128">-NsxtPassword</span></span>
<span data-ttu-id="14547-129">Tetszés szerint állítsa be a NSX-T kezelő jelszavát a privát felhő létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="14547-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="14547-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14547-130">-ResourceGroupName</span></span>
<span data-ttu-id="14547-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="14547-131">The name of the resource group.</span></span>
<span data-ttu-id="14547-132">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="14547-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="14547-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="14547-133">-Sku</span></span>
<span data-ttu-id="14547-134">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="14547-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="14547-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14547-135">-SubscriptionId</span></span>
<span data-ttu-id="14547-136">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="14547-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="14547-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="14547-137">-Tag</span></span>
<span data-ttu-id="14547-138">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="14547-138">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14547-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="14547-139">-VcenterPassword</span></span>
<span data-ttu-id="14547-140">Tetszés szerint állítsa be a vCenter rendszergazdai jelszavát a privát felhő létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="14547-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="14547-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="14547-141">-Confirm</span></span>
<span data-ttu-id="14547-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="14547-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14547-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14547-143">-WhatIf</span></span>
<span data-ttu-id="14547-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="14547-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14547-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14547-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14547-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14547-146">CommonParameters</span></span>
<span data-ttu-id="14547-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14547-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14547-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="14547-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14547-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14547-149">INPUTS</span></span>

## <span data-ttu-id="14547-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14547-150">OUTPUTS</span></span>

### <span data-ttu-id="14547-151">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="14547-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="14547-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14547-152">NOTES</span></span>

<span data-ttu-id="14547-153">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="14547-153">ALIASES</span></span>

## <span data-ttu-id="14547-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14547-154">RELATED LINKS</span></span>

