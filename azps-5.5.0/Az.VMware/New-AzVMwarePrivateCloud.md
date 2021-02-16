---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.VMware/new-azVMwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
ms.openlocfilehash: 3e5e8fa4d098ce68899294a25866b4636c80878e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155962"
---
# <span data-ttu-id="4660a-101">New-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="4660a-101">New-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="4660a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4660a-102">SYNOPSIS</span></span>
<span data-ttu-id="4660a-103">Privát felhő létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="4660a-103">Create or update a private cloud</span></span>

## <span data-ttu-id="4660a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4660a-104">SYNTAX</span></span>

```
New-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>] [-AcceptEULA]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4660a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4660a-105">DESCRIPTION</span></span>
<span data-ttu-id="4660a-106">Privát felhő létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="4660a-106">Create or update a private cloud</span></span>

## <span data-ttu-id="4660a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4660a-107">EXAMPLES</span></span>

### <span data-ttu-id="4660a-108">1. példa: Privát felhő létrehozása</span><span class="sxs-lookup"><span data-stu-id="4660a-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="4660a-109">Privát felhő létrehozása</span><span class="sxs-lookup"><span data-stu-id="4660a-109">Create private cloud</span></span>

## <span data-ttu-id="4660a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4660a-110">PARAMETERS</span></span>

### <span data-ttu-id="4660a-111">-AcceptEULA</span><span class="sxs-lookup"><span data-stu-id="4660a-111">-AcceptEULA</span></span>
<span data-ttu-id="4660a-112">Az AVS-rel kapcsolatos eula-k elfogadása, a jogi kifejezés előugró ablakként jelenik meg a paraméter megadása nélkül</span><span class="sxs-lookup"><span data-stu-id="4660a-112">Accept EULA of AVS, legal term will pop up without this parameter provided</span></span>

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

### <span data-ttu-id="4660a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4660a-113">-AsJob</span></span>
<span data-ttu-id="4660a-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="4660a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4660a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4660a-115">-DefaultProfile</span></span>
<span data-ttu-id="4660a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4660a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4660a-117">-Internet</span><span class="sxs-lookup"><span data-stu-id="4660a-117">-Internet</span></span>
<span data-ttu-id="4660a-118">Az internetkapcsolat be van kapcsolva vagy le van tiltva</span><span class="sxs-lookup"><span data-stu-id="4660a-118">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4660a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="4660a-119">-Location</span></span>
<span data-ttu-id="4660a-120">Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="4660a-120">Resource location</span></span>

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

### <span data-ttu-id="4660a-121">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="4660a-121">-ManagementClusterSize</span></span>
<span data-ttu-id="4660a-122">A fürt mérete</span><span class="sxs-lookup"><span data-stu-id="4660a-122">The cluster size</span></span>

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

### <span data-ttu-id="4660a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4660a-123">-Name</span></span>
<span data-ttu-id="4660a-124">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="4660a-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="4660a-125">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="4660a-125">-NetworkBlock</span></span>
<span data-ttu-id="4660a-126">A címblokknak egyedinek kell lennie az előfizetés VNet-hálózatában, valamint a webhelyen is.</span><span class="sxs-lookup"><span data-stu-id="4660a-126">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="4660a-127">Győződjön meg arról, hogy a CIDR formátum megfelel az (A.B.C.D/X) formátumnak, ahol az A,B,C,D 0 és 255 közötti, az X pedig 0 és 22 között van</span><span class="sxs-lookup"><span data-stu-id="4660a-127">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="4660a-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4660a-128">-NoWait</span></span>
<span data-ttu-id="4660a-129">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="4660a-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4660a-130">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="4660a-130">-NsxtPassword</span></span>
<span data-ttu-id="4660a-131">Szükség esetén állítsa be az NSX-T Manager jelszavát a privát felhő létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="4660a-131">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="4660a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4660a-132">-ResourceGroupName</span></span>
<span data-ttu-id="4660a-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4660a-133">The name of the resource group.</span></span>
<span data-ttu-id="4660a-134">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="4660a-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4660a-135">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="4660a-135">-Sku</span></span>
<span data-ttu-id="4660a-136">A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="4660a-136">The name of the SKU.</span></span>

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

### <span data-ttu-id="4660a-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4660a-137">-SubscriptionId</span></span>
<span data-ttu-id="4660a-138">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4660a-138">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4660a-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="4660a-139">-Tag</span></span>
<span data-ttu-id="4660a-140">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="4660a-140">Resource tags</span></span>

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

### <span data-ttu-id="4660a-141">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="4660a-141">-VcenterPassword</span></span>
<span data-ttu-id="4660a-142">Szükség esetén állítsa be a vCenter rendszergazdai jelszavát a privát felhő létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="4660a-142">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="4660a-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4660a-143">-Confirm</span></span>
<span data-ttu-id="4660a-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4660a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4660a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4660a-145">-WhatIf</span></span>
<span data-ttu-id="4660a-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4660a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4660a-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4660a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4660a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4660a-148">CommonParameters</span></span>
<span data-ttu-id="4660a-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4660a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4660a-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4660a-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4660a-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4660a-151">INPUTS</span></span>

## <span data-ttu-id="4660a-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4660a-152">OUTPUTS</span></span>

### <span data-ttu-id="4660a-153">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="4660a-153">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="4660a-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4660a-154">NOTES</span></span>

<span data-ttu-id="4660a-155">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4660a-155">ALIASES</span></span>

## <span data-ttu-id="4660a-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4660a-156">RELATED LINKS</span></span>

