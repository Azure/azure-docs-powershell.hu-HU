---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 3798590f3b4df738bc38231018adabf99ba39237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503827"
---
# <span data-ttu-id="ee2b5-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ee2b5-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="ee2b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee2b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2b5-103">Leállítja a VMSS vagy a virtuális gépeket a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee2b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee2b5-104">SYNTAX</span></span>

### <span data-ttu-id="ee2b5-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee2b5-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2b5-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ee2b5-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee2b5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee2b5-107">DESCRIPTION</span></span>
<span data-ttu-id="ee2b5-108">A **stop-AzureRmVmss** parancsmag a Virtual Machine Scale set (VMSS) vagy a virtuális gépek egy halmazán belül minden virtuális gépet leállítja.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="ee2b5-109">A *InstanceId* paraméterrel kiválaszthatja a virtuális gépek halmazát.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="ee2b5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ee2b5-110">EXAMPLES</span></span>

### <span data-ttu-id="ee2b5-111">1. példa: az összes virtuális gép leállítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="ee2b5-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ee2b5-112">Ez a parancs a ContosoVMSS nevű VMSS tartozó összes virtuális gépet leállítja.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="ee2b5-113">2. példa: a virtuális gépek meghatározott halmazának leállítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="ee2b5-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="ee2b5-114">Ez a parancs a ContosoVMSS nevű VMSS tartozó példánynév-karakterlánc tömbben meghatározott virtuális gépek meghatározott halmazát leállítja.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="ee2b5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee2b5-115">PARAMETERS</span></span>

### <span data-ttu-id="ee2b5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ee2b5-116">-Force</span></span>
<span data-ttu-id="ee2b5-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee2b5-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="ee2b5-118">-InstanceId</span></span>
<span data-ttu-id="ee2b5-119">Karakterláncként adja meg azt a virtuális gép-példányok AZONOSÍTÓját vagy azonosítóit, amelyekre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-119">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="ee2b5-120">Például: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="ee2b5-120">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee2b5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee2b5-121">-ResourceGroupName</span></span>
<span data-ttu-id="ee2b5-122">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-122">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee2b5-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="ee2b5-123">-StayProvisioned</span></span>
<span data-ttu-id="ee2b5-124">Ha meg van adva, a virtuális gép bekapcsolja a leállítási állapotot.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-124">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="ee2b5-125">Ha nem adja meg, a virtuális gép beírja a leállított kihagyott állapotot.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-125">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="ee2b5-126">A rendszer továbbra is terheli a VMs-et a leállított állapotban, de nem a VMs esetében a leállított állapotban.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-126">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee2b5-127">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ee2b5-127">-VMScaleSetName</span></span>
<span data-ttu-id="ee2b5-128">Annak a VMSS a nevét adja meg, amelyhez ez a parancsmag leállítja a virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-128">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee2b5-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee2b5-129">-Confirm</span></span>
<span data-ttu-id="ee2b5-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee2b5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee2b5-131">-WhatIf</span></span>
<span data-ttu-id="ee2b5-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee2b5-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee2b5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2b5-134">CommonParameters</span></span>
<span data-ttu-id="ee2b5-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee2b5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2b5-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee2b5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2b5-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee2b5-137">INPUTS</span></span>

### <span data-ttu-id="ee2b5-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="ee2b5-138">None</span></span>
<span data-ttu-id="ee2b5-139">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ee2b5-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee2b5-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee2b5-140">OUTPUTS</span></span>

## <span data-ttu-id="ee2b5-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee2b5-141">NOTES</span></span>

## <span data-ttu-id="ee2b5-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee2b5-142">RELATED LINKS</span></span>

[<span data-ttu-id="ee2b5-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ee2b5-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="ee2b5-144">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ee2b5-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="ee2b5-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ee2b5-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="ee2b5-146">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ee2b5-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="ee2b5-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ee2b5-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="ee2b5-148">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ee2b5-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="ee2b5-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ee2b5-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


