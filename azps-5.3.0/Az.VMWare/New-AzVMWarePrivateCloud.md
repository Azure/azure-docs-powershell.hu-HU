---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467058"
---
# <span data-ttu-id="ab307-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="ab307-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="ab307-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab307-102">SYNOPSIS</span></span>
<span data-ttu-id="ab307-103">Privát felhő létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="ab307-103">Create or update a private cloud</span></span>

## <span data-ttu-id="ab307-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ab307-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ab307-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ab307-105">DESCRIPTION</span></span>
<span data-ttu-id="ab307-106">Privát felhő létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="ab307-106">Create or update a private cloud</span></span>

## <span data-ttu-id="ab307-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ab307-107">EXAMPLES</span></span>

### <span data-ttu-id="ab307-108">1. példa: Privát felhő létrehozása</span><span class="sxs-lookup"><span data-stu-id="ab307-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="ab307-109">Privát felhő létrehozása</span><span class="sxs-lookup"><span data-stu-id="ab307-109">Create private cloud</span></span>

## <span data-ttu-id="ab307-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab307-110">PARAMETERS</span></span>

### <span data-ttu-id="ab307-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab307-111">-AsJob</span></span>
<span data-ttu-id="ab307-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="ab307-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ab307-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab307-113">-DefaultProfile</span></span>
<span data-ttu-id="ab307-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab307-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab307-115">-Internet</span><span class="sxs-lookup"><span data-stu-id="ab307-115">-Internet</span></span>
<span data-ttu-id="ab307-116">Az internetkapcsolat be van kapcsolva vagy le van tiltva</span><span class="sxs-lookup"><span data-stu-id="ab307-116">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="ab307-117">-Location</span><span class="sxs-lookup"><span data-stu-id="ab307-117">-Location</span></span>
<span data-ttu-id="ab307-118">Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="ab307-118">Resource location</span></span>

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

### <span data-ttu-id="ab307-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="ab307-119">-ManagementClusterSize</span></span>
<span data-ttu-id="ab307-120">A fürt mérete</span><span class="sxs-lookup"><span data-stu-id="ab307-120">The cluster size</span></span>

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

### <span data-ttu-id="ab307-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ab307-121">-Name</span></span>
<span data-ttu-id="ab307-122">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="ab307-122">Name of the private cloud</span></span>

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

### <span data-ttu-id="ab307-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="ab307-123">-NetworkBlock</span></span>
<span data-ttu-id="ab307-124">A címblokknak egyedinek kell lennie az előfizetés VNet-hálózatában és a webhelyen is.</span><span class="sxs-lookup"><span data-stu-id="ab307-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="ab307-125">Győződjön meg arról, hogy a CIDR formátum megfelel az (A.B.C.D/X) formátumnak, ahol az A,B,C,D 0 és 255 közötti, az X pedig 0 és 22 között van</span><span class="sxs-lookup"><span data-stu-id="ab307-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="ab307-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ab307-126">-NoWait</span></span>
<span data-ttu-id="ab307-127">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="ab307-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ab307-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="ab307-128">-NsxtPassword</span></span>
<span data-ttu-id="ab307-129">Szükség esetén állítsa be az NSX-T Manager jelszavát a privát felhő létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="ab307-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="ab307-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab307-130">-ResourceGroupName</span></span>
<span data-ttu-id="ab307-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ab307-131">The name of the resource group.</span></span>
<span data-ttu-id="ab307-132">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="ab307-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ab307-133">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="ab307-133">-Sku</span></span>
<span data-ttu-id="ab307-134">A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="ab307-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="ab307-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab307-135">-SubscriptionId</span></span>
<span data-ttu-id="ab307-136">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ab307-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ab307-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="ab307-137">-Tag</span></span>
<span data-ttu-id="ab307-138">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="ab307-138">Resource tags</span></span>

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

### <span data-ttu-id="ab307-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="ab307-139">-VcenterPassword</span></span>
<span data-ttu-id="ab307-140">Szükség esetén állítsa be a vCenter rendszergazdai jelszavát a privát felhő létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="ab307-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="ab307-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab307-141">-Confirm</span></span>
<span data-ttu-id="ab307-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ab307-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab307-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab307-143">-WhatIf</span></span>
<span data-ttu-id="ab307-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ab307-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab307-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ab307-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab307-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab307-146">CommonParameters</span></span>
<span data-ttu-id="ab307-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab307-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab307-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab307-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab307-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab307-149">INPUTS</span></span>

## <span data-ttu-id="ab307-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab307-150">OUTPUTS</span></span>

### <span data-ttu-id="ab307-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="ab307-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="ab307-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ab307-152">NOTES</span></span>

<span data-ttu-id="ab307-153">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ab307-153">ALIASES</span></span>

## <span data-ttu-id="ab307-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab307-154">RELATED LINKS</span></span>

