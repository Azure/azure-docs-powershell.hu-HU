---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 1fdd45c36d085b376ed900f0054dd98bc28c7525
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667180"
---
# <span data-ttu-id="34100-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="34100-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="34100-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34100-102">SYNOPSIS</span></span>
<span data-ttu-id="34100-103">Módosítja egy VMSS-példány állapotát.</span><span class="sxs-lookup"><span data-stu-id="34100-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="34100-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34100-104">SYNTAX</span></span>

### <span data-ttu-id="34100-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="34100-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34100-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="34100-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34100-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="34100-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34100-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="34100-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34100-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="34100-109">DESCRIPTION</span></span>
<span data-ttu-id="34100-110">A **set-AzVmssVM** parancsmag a virtuálisgép-készlet (VMSS) példány állapotát módosítja.</span><span class="sxs-lookup"><span data-stu-id="34100-110">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="34100-111">Példák</span><span class="sxs-lookup"><span data-stu-id="34100-111">EXAMPLES</span></span>

## <span data-ttu-id="34100-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34100-112">PARAMETERS</span></span>

### <span data-ttu-id="34100-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34100-113">-AsJob</span></span>
<span data-ttu-id="34100-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="34100-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34100-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34100-115">-DefaultProfile</span></span>
<span data-ttu-id="34100-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34100-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34100-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="34100-117">-InstanceId</span></span>
<span data-ttu-id="34100-118">Annak az VMSS-példánynak az AZONOSÍTÓját adja meg, amelyre ez a parancsmag módosítja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="34100-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="34100-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="34100-119">-PerformMaintenance</span></span>
<span data-ttu-id="34100-120">Azt jelzi, hogy ez a parancsmag karbantartást hajt végre egy virtuális gépen a VMSS.</span><span class="sxs-lookup"><span data-stu-id="34100-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="34100-121">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="34100-121">-Redeploy</span></span>
<span data-ttu-id="34100-122">Azt jelzi, hogy ez a parancsmag áttelepíti a virtuális gépet a VMSS.</span><span class="sxs-lookup"><span data-stu-id="34100-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="34100-123">-Reimage</span><span class="sxs-lookup"><span data-stu-id="34100-123">-Reimage</span></span>
<span data-ttu-id="34100-124">Jelzi, hogy ez a parancsmag átadja a VMSS-példányt.</span><span class="sxs-lookup"><span data-stu-id="34100-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="34100-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="34100-125">-ReimageAll</span></span>
<span data-ttu-id="34100-126">Jelzi, hogy a parancsmag a VMSS példány összes lemezét átadja.</span><span class="sxs-lookup"><span data-stu-id="34100-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="34100-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34100-127">-ResourceGroupName</span></span>
<span data-ttu-id="34100-128">A VMSS-példányt tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="34100-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="34100-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="34100-129">-VMScaleSetName</span></span>
<span data-ttu-id="34100-130">A parancsmag által módosított VMSS-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="34100-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="34100-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="34100-131">-Confirm</span></span>
<span data-ttu-id="34100-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="34100-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34100-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34100-133">-WhatIf</span></span>
<span data-ttu-id="34100-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="34100-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34100-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="34100-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34100-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34100-136">CommonParameters</span></span>
<span data-ttu-id="34100-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34100-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34100-138">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="34100-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34100-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34100-139">INPUTS</span></span>

### <span data-ttu-id="34100-140">System. String</span><span class="sxs-lookup"><span data-stu-id="34100-140">System.String</span></span>

## <span data-ttu-id="34100-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34100-141">OUTPUTS</span></span>

### <span data-ttu-id="34100-142">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="34100-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="34100-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34100-143">NOTES</span></span>

## <span data-ttu-id="34100-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34100-144">RELATED LINKS</span></span>

[<span data-ttu-id="34100-145">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="34100-145">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
