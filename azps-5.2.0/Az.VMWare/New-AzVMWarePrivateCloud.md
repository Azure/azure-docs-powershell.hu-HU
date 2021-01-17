---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332850"
---
# <span data-ttu-id="213c0-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="213c0-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="213c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="213c0-102">SYNOPSIS</span></span>
<span data-ttu-id="213c0-103">Privát felhő létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="213c0-103">Create or update a private cloud</span></span>

## <span data-ttu-id="213c0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="213c0-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="213c0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="213c0-105">DESCRIPTION</span></span>
<span data-ttu-id="213c0-106">Privát felhő létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="213c0-106">Create or update a private cloud</span></span>

## <span data-ttu-id="213c0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="213c0-107">EXAMPLES</span></span>

### <span data-ttu-id="213c0-108">1. példa: Privát felhő létrehozása</span><span class="sxs-lookup"><span data-stu-id="213c0-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="213c0-109">Privát felhő létrehozása</span><span class="sxs-lookup"><span data-stu-id="213c0-109">Create private cloud</span></span>

## <span data-ttu-id="213c0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="213c0-110">PARAMETERS</span></span>

### <span data-ttu-id="213c0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="213c0-111">-AsJob</span></span>
<span data-ttu-id="213c0-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="213c0-112">Run the command as a job</span></span>

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

### <span data-ttu-id="213c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="213c0-113">-DefaultProfile</span></span>
<span data-ttu-id="213c0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="213c0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="213c0-115">-Internet</span><span class="sxs-lookup"><span data-stu-id="213c0-115">-Internet</span></span>
<span data-ttu-id="213c0-116">Az internetkapcsolat be van kapcsolva vagy le van tiltva</span><span class="sxs-lookup"><span data-stu-id="213c0-116">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="213c0-117">-Location</span><span class="sxs-lookup"><span data-stu-id="213c0-117">-Location</span></span>
<span data-ttu-id="213c0-118">Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="213c0-118">Resource location</span></span>

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

### <span data-ttu-id="213c0-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="213c0-119">-ManagementClusterSize</span></span>
<span data-ttu-id="213c0-120">A fürt mérete</span><span class="sxs-lookup"><span data-stu-id="213c0-120">The cluster size</span></span>

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

### <span data-ttu-id="213c0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="213c0-121">-Name</span></span>
<span data-ttu-id="213c0-122">A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="213c0-122">Name of the private cloud</span></span>

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

### <span data-ttu-id="213c0-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="213c0-123">-NetworkBlock</span></span>
<span data-ttu-id="213c0-124">A címblokknak egyedinek kell lennie az előfizetés VNet-hálózatában és a webhelyen is.</span><span class="sxs-lookup"><span data-stu-id="213c0-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="213c0-125">Győződjön meg arról, hogy a CIDR formátum megfeleltetve (A.B.C.D/X), ahol az A,B,C,D 0 és 255 között van, az X pedig 0 és 22 között van</span><span class="sxs-lookup"><span data-stu-id="213c0-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="213c0-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="213c0-126">-NoWait</span></span>
<span data-ttu-id="213c0-127">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="213c0-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="213c0-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="213c0-128">-NsxtPassword</span></span>
<span data-ttu-id="213c0-129">Szükség esetén állítsa be az NSX-T Manager jelszavát a privát felhő létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="213c0-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="213c0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="213c0-130">-ResourceGroupName</span></span>
<span data-ttu-id="213c0-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="213c0-131">The name of the resource group.</span></span>
<span data-ttu-id="213c0-132">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="213c0-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="213c0-133">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="213c0-133">-Sku</span></span>
<span data-ttu-id="213c0-134">A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="213c0-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="213c0-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="213c0-135">-SubscriptionId</span></span>
<span data-ttu-id="213c0-136">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="213c0-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="213c0-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="213c0-137">-Tag</span></span>
<span data-ttu-id="213c0-138">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="213c0-138">Resource tags</span></span>

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

### <span data-ttu-id="213c0-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="213c0-139">-VcenterPassword</span></span>
<span data-ttu-id="213c0-140">Szükség esetén állítsa be a vCenter rendszergazdai jelszavát a privát felhő létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="213c0-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="213c0-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="213c0-141">-Confirm</span></span>
<span data-ttu-id="213c0-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="213c0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="213c0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="213c0-143">-WhatIf</span></span>
<span data-ttu-id="213c0-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="213c0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="213c0-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="213c0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="213c0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="213c0-146">CommonParameters</span></span>
<span data-ttu-id="213c0-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="213c0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="213c0-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="213c0-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="213c0-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="213c0-149">INPUTS</span></span>

## <span data-ttu-id="213c0-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="213c0-150">OUTPUTS</span></span>

### <span data-ttu-id="213c0-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="213c0-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="213c0-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="213c0-152">NOTES</span></span>

<span data-ttu-id="213c0-153">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="213c0-153">ALIASES</span></span>

## <span data-ttu-id="213c0-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="213c0-154">RELATED LINKS</span></span>

