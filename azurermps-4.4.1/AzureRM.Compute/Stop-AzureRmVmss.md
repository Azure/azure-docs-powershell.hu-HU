---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 11b387e4022bce98e1275bb2af09bc97beff0041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673125"
---
# <span data-ttu-id="81c82-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81c82-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="81c82-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81c82-102">SYNOPSIS</span></span>
<span data-ttu-id="81c82-103">Leállítja a VMSS vagy a virtuális gépeket a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="81c82-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81c82-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81c82-104">SYNTAX</span></span>

### <span data-ttu-id="81c82-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81c82-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81c82-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="81c82-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81c82-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="81c82-107">DESCRIPTION</span></span>
<span data-ttu-id="81c82-108">A **stop-AzureRmVmss** parancsmag a Virtual Machine Scale set (VMSS) vagy a virtuális gépek egy halmazán belül minden virtuális gépet leállítja.</span><span class="sxs-lookup"><span data-stu-id="81c82-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="81c82-109">A *InstanceId* paraméterrel kiválaszthatja a virtuális gépek halmazát.</span><span class="sxs-lookup"><span data-stu-id="81c82-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="81c82-110">Példák</span><span class="sxs-lookup"><span data-stu-id="81c82-110">EXAMPLES</span></span>

### <span data-ttu-id="81c82-111">1. példa: az összes virtuális gép leállítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="81c82-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="81c82-112">Ez a parancs a ContosoVMSS nevű VMSS tartozó összes virtuális gépet leállítja.</span><span class="sxs-lookup"><span data-stu-id="81c82-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="81c82-113">2. példa: a virtuális gépek meghatározott halmazának leállítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="81c82-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="81c82-114">Ez a parancs a ContosoVMSS nevű VMSS tartozó példánynév-karakterlánc tömbben meghatározott virtuális gépek meghatározott halmazát leállítja.</span><span class="sxs-lookup"><span data-stu-id="81c82-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="81c82-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81c82-115">PARAMETERS</span></span>

### <span data-ttu-id="81c82-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c82-116">-DefaultProfile</span></span>
<span data-ttu-id="81c82-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81c82-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81c82-118">-Force</span><span class="sxs-lookup"><span data-stu-id="81c82-118">-Force</span></span>
<span data-ttu-id="81c82-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="81c82-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="81c82-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="81c82-120">-InstanceId</span></span>
<span data-ttu-id="81c82-121">Karakterláncként adja meg azt a virtuális gép-példányok AZONOSÍTÓját vagy azonosítóit, amelyekre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="81c82-121">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="81c82-122">Például: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="81c82-122">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81c82-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81c82-123">-ResourceGroupName</span></span>
<span data-ttu-id="81c82-124">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81c82-124">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="81c82-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="81c82-125">-StayProvisioned</span></span>
<span data-ttu-id="81c82-126">Ha meg van adva, a virtuális gép bekapcsolja a leállítási állapotot.</span><span class="sxs-lookup"><span data-stu-id="81c82-126">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="81c82-127">Ha nem adja meg, a virtuális gép beírja a leállított kihagyott állapotot.</span><span class="sxs-lookup"><span data-stu-id="81c82-127">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="81c82-128">A rendszer továbbra is terheli a VMs-et a leállított állapotban, de nem a VMs esetében a leállított állapotban.</span><span class="sxs-lookup"><span data-stu-id="81c82-128">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


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

### <span data-ttu-id="81c82-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="81c82-129">-VMScaleSetName</span></span>
<span data-ttu-id="81c82-130">Annak a VMSS a nevét adja meg, amelyhez ez a parancsmag leállítja a virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="81c82-130">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="81c82-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81c82-131">-Confirm</span></span>
<span data-ttu-id="81c82-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81c82-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81c82-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81c82-133">-WhatIf</span></span>
<span data-ttu-id="81c82-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81c82-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81c82-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81c82-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81c82-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c82-136">CommonParameters</span></span>
<span data-ttu-id="81c82-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81c82-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c82-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81c82-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c82-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81c82-139">INPUTS</span></span>

## <span data-ttu-id="81c82-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81c82-140">OUTPUTS</span></span>

## <span data-ttu-id="81c82-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81c82-141">NOTES</span></span>

## <span data-ttu-id="81c82-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81c82-142">RELATED LINKS</span></span>

[<span data-ttu-id="81c82-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81c82-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="81c82-144">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81c82-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="81c82-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81c82-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="81c82-146">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81c82-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="81c82-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81c82-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="81c82-148">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81c82-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="81c82-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81c82-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


