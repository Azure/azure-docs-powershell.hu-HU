---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 32e04fb16d0e3360abb22177e453d5d629dbb098
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014607"
---
# <span data-ttu-id="10021-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="10021-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="10021-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10021-102">SYNOPSIS</span></span>
<span data-ttu-id="10021-103">Módosítja egy VMSS-példány állapotát.</span><span class="sxs-lookup"><span data-stu-id="10021-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="10021-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10021-104">SYNTAX</span></span>

### <span data-ttu-id="10021-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10021-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10021-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="10021-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10021-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="10021-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10021-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="10021-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10021-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="10021-109">DESCRIPTION</span></span>
<span data-ttu-id="10021-110">A **set-AzVmssVM** parancsmag a virtuálisgép-készlet (VMSS) példány állapotát módosítja.</span><span class="sxs-lookup"><span data-stu-id="10021-110">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="10021-111">Példák</span><span class="sxs-lookup"><span data-stu-id="10021-111">EXAMPLES</span></span>

## <span data-ttu-id="10021-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10021-112">PARAMETERS</span></span>

### <span data-ttu-id="10021-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10021-113">-AsJob</span></span>
<span data-ttu-id="10021-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="10021-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10021-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10021-115">-DefaultProfile</span></span>
<span data-ttu-id="10021-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10021-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10021-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="10021-117">-InstanceId</span></span>
<span data-ttu-id="10021-118">Annak az VMSS-példánynak az AZONOSÍTÓját adja meg, amelyre ez a parancsmag módosítja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="10021-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10021-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="10021-119">-PerformMaintenance</span></span>
<span data-ttu-id="10021-120">Azt jelzi, hogy ez a parancsmag karbantartást hajt végre egy virtuális gépen a VMSS.</span><span class="sxs-lookup"><span data-stu-id="10021-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10021-121">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="10021-121">-Redeploy</span></span>
<span data-ttu-id="10021-122">Azt jelzi, hogy ez a parancsmag áttelepíti a virtuális gépet a VMSS.</span><span class="sxs-lookup"><span data-stu-id="10021-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10021-123">-Reimage</span><span class="sxs-lookup"><span data-stu-id="10021-123">-Reimage</span></span>
<span data-ttu-id="10021-124">Jelzi, hogy ez a parancsmag átadja a VMSS-példányt.</span><span class="sxs-lookup"><span data-stu-id="10021-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10021-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="10021-125">-ReimageAll</span></span>
<span data-ttu-id="10021-126">Jelzi, hogy a parancsmag a VMSS példány összes lemezét átadja.</span><span class="sxs-lookup"><span data-stu-id="10021-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10021-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10021-127">-ResourceGroupName</span></span>
<span data-ttu-id="10021-128">A VMSS-példányt tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10021-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10021-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="10021-129">-VMScaleSetName</span></span>
<span data-ttu-id="10021-130">A parancsmag által módosított VMSS-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10021-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10021-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="10021-131">-Confirm</span></span>
<span data-ttu-id="10021-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="10021-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10021-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10021-133">-WhatIf</span></span>
<span data-ttu-id="10021-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="10021-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10021-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="10021-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10021-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10021-136">CommonParameters</span></span>
<span data-ttu-id="10021-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10021-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10021-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="10021-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10021-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10021-139">INPUTS</span></span>

### <span data-ttu-id="10021-140">System. String</span><span class="sxs-lookup"><span data-stu-id="10021-140">System.String</span></span>

## <span data-ttu-id="10021-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10021-141">OUTPUTS</span></span>

### <span data-ttu-id="10021-142">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="10021-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="10021-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10021-143">NOTES</span></span>

## <span data-ttu-id="10021-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10021-144">RELATED LINKS</span></span>

[<span data-ttu-id="10021-145">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="10021-145">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
