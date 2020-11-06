---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: f71e827769015b7abe4d503064d97ec1d3c1228b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502183"
---
# <span data-ttu-id="55597-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="55597-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="55597-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55597-102">SYNOPSIS</span></span>
<span data-ttu-id="55597-103">Módosítja egy VMSS-példány állapotát.</span><span class="sxs-lookup"><span data-stu-id="55597-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55597-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55597-104">SYNTAX</span></span>

### <span data-ttu-id="55597-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55597-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55597-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="55597-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55597-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="55597-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55597-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="55597-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55597-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="55597-109">DESCRIPTION</span></span>
<span data-ttu-id="55597-110">A **set-AzureRmVmssVM** parancsmag a virtuálisgép-készlet (VMSS) példány állapotát módosítja.</span><span class="sxs-lookup"><span data-stu-id="55597-110">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="55597-111">Példák</span><span class="sxs-lookup"><span data-stu-id="55597-111">EXAMPLES</span></span>

## <span data-ttu-id="55597-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55597-112">PARAMETERS</span></span>

### <span data-ttu-id="55597-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55597-113">-AsJob</span></span>
<span data-ttu-id="55597-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="55597-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55597-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55597-115">-DefaultProfile</span></span>
<span data-ttu-id="55597-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55597-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55597-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="55597-117">-InstanceId</span></span>
<span data-ttu-id="55597-118">Annak az VMSS-példánynak az AZONOSÍTÓját adja meg, amelyre ez a parancsmag módosítja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="55597-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55597-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="55597-119">-PerformMaintenance</span></span>
<span data-ttu-id="55597-120">Azt jelzi, hogy ez a parancsmag karbantartást hajt végre egy virtuális gépen a VMSS.</span><span class="sxs-lookup"><span data-stu-id="55597-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="55597-121">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="55597-121">-Redeploy</span></span>
<span data-ttu-id="55597-122">Azt jelzi, hogy ez a parancsmag áttelepíti a virtuális gépet a VMSS.</span><span class="sxs-lookup"><span data-stu-id="55597-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="55597-123">-Reimage</span><span class="sxs-lookup"><span data-stu-id="55597-123">-Reimage</span></span>
<span data-ttu-id="55597-124">Jelzi, hogy ez a parancsmag átadja a VMSS-példányt.</span><span class="sxs-lookup"><span data-stu-id="55597-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="55597-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="55597-125">-ReimageAll</span></span>
<span data-ttu-id="55597-126">Jelzi, hogy a parancsmag a VMSS példány összes lemezét átadja.</span><span class="sxs-lookup"><span data-stu-id="55597-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="55597-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55597-127">-ResourceGroupName</span></span>
<span data-ttu-id="55597-128">A VMSS-példányt tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55597-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55597-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="55597-129">-VMScaleSetName</span></span>
<span data-ttu-id="55597-130">A parancsmag által módosított VMSS-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55597-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55597-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="55597-131">-Confirm</span></span>
<span data-ttu-id="55597-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="55597-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55597-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55597-133">-WhatIf</span></span>
<span data-ttu-id="55597-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="55597-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55597-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55597-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55597-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55597-136">CommonParameters</span></span>
<span data-ttu-id="55597-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55597-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55597-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55597-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55597-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55597-139">INPUTS</span></span>

### <span data-ttu-id="55597-140">System. String</span><span class="sxs-lookup"><span data-stu-id="55597-140">System.String</span></span>

## <span data-ttu-id="55597-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55597-141">OUTPUTS</span></span>

### <span data-ttu-id="55597-142">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="55597-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="55597-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55597-143">NOTES</span></span>

## <span data-ttu-id="55597-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55597-144">RELATED LINKS</span></span>

[<span data-ttu-id="55597-145">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="55597-145">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
