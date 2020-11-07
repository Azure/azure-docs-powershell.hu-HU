---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 50fd6447448968527b942e163f520142f594b7a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848861"
---
# <span data-ttu-id="74e1b-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="74e1b-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="74e1b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="74e1b-103">Leállítja a VMSS vagy a virtuális gépeket a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="74e1b-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74e1b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74e1b-104">SYNTAX</span></span>

### <span data-ttu-id="74e1b-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74e1b-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74e1b-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="74e1b-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74e1b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="74e1b-107">DESCRIPTION</span></span>
<span data-ttu-id="74e1b-108">A **stop-AzureRmVmss** parancsmag a Virtual Machine Scale set (VMSS) vagy a virtuális gépek egy halmazán belül minden virtuális gépet leállítja.</span><span class="sxs-lookup"><span data-stu-id="74e1b-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="74e1b-109">A *InstanceId* paraméterrel kiválaszthatja a virtuális gépek halmazát.</span><span class="sxs-lookup"><span data-stu-id="74e1b-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="74e1b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="74e1b-110">EXAMPLES</span></span>

### <span data-ttu-id="74e1b-111">1. példa: az összes virtuális gép leállítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="74e1b-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="74e1b-112">Ez a parancs a ContosoVMSS nevű VMSS tartozó összes virtuális gépet leállítja.</span><span class="sxs-lookup"><span data-stu-id="74e1b-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="74e1b-113">2. példa: a virtuális gépek meghatározott halmazának leállítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="74e1b-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="74e1b-114">Ez a parancs a ContosoVMSS nevű VMSS tartozó példánynév-karakterlánc tömbben meghatározott virtuális gépek meghatározott halmazát leállítja.</span><span class="sxs-lookup"><span data-stu-id="74e1b-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="74e1b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74e1b-115">PARAMETERS</span></span>

### <span data-ttu-id="74e1b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74e1b-116">-AsJob</span></span>
<span data-ttu-id="74e1b-117">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="74e1b-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74e1b-118">-DefaultProfile</span></span>
<span data-ttu-id="74e1b-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74e1b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e1b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="74e1b-120">-Force</span></span>
<span data-ttu-id="74e1b-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="74e1b-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e1b-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="74e1b-122">-InstanceId</span></span>
<span data-ttu-id="74e1b-123">Karakterláncként adja meg azt a virtuális gép-példányok AZONOSÍTÓját vagy azonosítóit, amelyekre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="74e1b-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="74e1b-124">Például: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="74e1b-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="74e1b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74e1b-125">-ResourceGroupName</span></span>
<span data-ttu-id="74e1b-126">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="74e1b-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="74e1b-127">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="74e1b-127">-StayProvisioned</span></span>
<span data-ttu-id="74e1b-128">Ha meg van adva, a virtuális gép bekapcsolja a leállítási állapotot.</span><span class="sxs-lookup"><span data-stu-id="74e1b-128">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="74e1b-129">Ha nem adja meg, a virtuális gép beírja a leállított kihagyott állapotot.</span><span class="sxs-lookup"><span data-stu-id="74e1b-129">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="74e1b-130">A rendszer továbbra is terheli a VMs-et a leállított állapotban, de nem a VMs esetében a leállított állapotban.</span><span class="sxs-lookup"><span data-stu-id="74e1b-130">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e1b-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="74e1b-131">-VMScaleSetName</span></span>
<span data-ttu-id="74e1b-132">Annak a VMSS a nevét adja meg, amelyhez ez a parancsmag leállítja a virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="74e1b-132">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="74e1b-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="74e1b-133">-Confirm</span></span>
<span data-ttu-id="74e1b-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74e1b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74e1b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74e1b-135">-WhatIf</span></span>
<span data-ttu-id="74e1b-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="74e1b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74e1b-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74e1b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74e1b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e1b-138">CommonParameters</span></span>
<span data-ttu-id="74e1b-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74e1b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e1b-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74e1b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e1b-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74e1b-141">INPUTS</span></span>

### <span data-ttu-id="74e1b-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="74e1b-142">None</span></span>
<span data-ttu-id="74e1b-143">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="74e1b-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="74e1b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74e1b-144">OUTPUTS</span></span>

### <span data-ttu-id="74e1b-145">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="74e1b-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="74e1b-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74e1b-146">NOTES</span></span>

## <span data-ttu-id="74e1b-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74e1b-147">RELATED LINKS</span></span>

[<span data-ttu-id="74e1b-148">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="74e1b-148">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="74e1b-149">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="74e1b-149">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="74e1b-150">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="74e1b-150">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="74e1b-151">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="74e1b-151">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="74e1b-152">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="74e1b-152">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="74e1b-153">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="74e1b-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="74e1b-154">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="74e1b-154">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


