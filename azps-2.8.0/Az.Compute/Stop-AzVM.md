---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: d0895fc436f4f7d59a4d9f5b6cfc18574d7e8d9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667176"
---
# <span data-ttu-id="cc622-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="cc622-101">Stop-AzVM</span></span>

## <span data-ttu-id="cc622-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc622-102">SYNOPSIS</span></span>
<span data-ttu-id="cc622-103">Azure virtuális gép leállítása</span><span class="sxs-lookup"><span data-stu-id="cc622-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="cc622-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc622-104">SYNTAX</span></span>

### <span data-ttu-id="cc622-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc622-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc622-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="cc622-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc622-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc622-107">DESCRIPTION</span></span>
<span data-ttu-id="cc622-108">A **stop-AzVM** parancsmag leállítja az Azure Virtual machinet.</span><span class="sxs-lookup"><span data-stu-id="cc622-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="cc622-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cc622-109">EXAMPLES</span></span>

### <span data-ttu-id="cc622-110">Példa 1: virtuális gép leállítása</span><span class="sxs-lookup"><span data-stu-id="cc622-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="cc622-111">Ez a parancs leállítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cc622-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="cc622-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc622-112">PARAMETERS</span></span>

### <span data-ttu-id="cc622-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc622-113">-AsJob</span></span>
<span data-ttu-id="cc622-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="cc622-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cc622-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc622-115">-DefaultProfile</span></span>
<span data-ttu-id="cc622-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc622-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc622-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cc622-117">-Force</span></span>
<span data-ttu-id="cc622-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="cc622-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc622-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="cc622-119">-Id</span></span>
<span data-ttu-id="cc622-120">A virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cc622-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc622-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc622-121">-Name</span></span>
<span data-ttu-id="cc622-122">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="cc622-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc622-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="cc622-123">-NoWait</span></span>
<span data-ttu-id="cc622-124">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="cc622-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="cc622-125">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="cc622-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cc622-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc622-126">-ResourceGroupName</span></span>
<span data-ttu-id="cc622-127">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc622-127">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc622-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="cc622-128">-SkipShutdown</span></span>
<span data-ttu-id="cc622-129">Ha nem kecses VM-leállítást szeretne igényelni a VM kiépített állapotban való megtartásakor.</span><span class="sxs-lookup"><span data-stu-id="cc622-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="cc622-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="cc622-130">-StayProvisioned</span></span>
<span data-ttu-id="cc622-131">A parancsmag leállítja az összes virtuális gépet a VMSS, de nem osztja fel őket.</span><span class="sxs-lookup"><span data-stu-id="cc622-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="cc622-132">A rendszer a leállított virtuális gépek számláját terheli.</span><span class="sxs-lookup"><span data-stu-id="cc622-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="cc622-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc622-133">-Confirm</span></span>
<span data-ttu-id="cc622-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc622-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc622-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc622-135">-WhatIf</span></span>
<span data-ttu-id="cc622-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc622-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc622-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc622-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc622-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc622-138">CommonParameters</span></span>
<span data-ttu-id="cc622-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc622-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc622-140">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cc622-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc622-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc622-141">INPUTS</span></span>

### <span data-ttu-id="cc622-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cc622-142">System.String</span></span>

## <span data-ttu-id="cc622-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc622-143">OUTPUTS</span></span>

### <span data-ttu-id="cc622-144">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="cc622-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="cc622-145">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cc622-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cc622-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc622-146">NOTES</span></span>

## <span data-ttu-id="cc622-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc622-147">RELATED LINKS</span></span>

[<span data-ttu-id="cc622-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="cc622-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="cc622-149">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="cc622-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="cc622-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="cc622-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="cc622-151">Újraindítás – AzVM</span><span class="sxs-lookup"><span data-stu-id="cc622-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="cc622-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="cc622-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="cc622-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="cc622-153">Update-AzVM</span></span>](./Update-AzVM.md)


