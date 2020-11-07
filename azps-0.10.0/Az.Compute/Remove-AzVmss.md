---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: c8de667ae818749e980d3e917838717ec3c85b07
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844357"
---
# <span data-ttu-id="a6edd-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6edd-101">Remove-AzVmss</span></span>

## <span data-ttu-id="a6edd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6edd-102">SYNOPSIS</span></span>
<span data-ttu-id="a6edd-103">Eltávolítja a VMSS belüli VMSS vagy virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="a6edd-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="a6edd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6edd-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6edd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6edd-105">DESCRIPTION</span></span>
<span data-ttu-id="a6edd-106">A **Remove-AzVmss** parancsmag eltávolítja a virtuális gép méretarányát (VMSS) az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="a6edd-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="a6edd-107">Ez a parancsmag a VMSS belül egy adott virtuális gép eltávolítására is használható.</span><span class="sxs-lookup"><span data-stu-id="a6edd-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="a6edd-108">A *InstanceId* paraméterrel eltávolíthatja egy adott virtuális GÉPET a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="a6edd-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="a6edd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a6edd-109">EXAMPLES</span></span>

### <span data-ttu-id="a6edd-110">1. példa: VMSS eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a6edd-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="a6edd-111">Ez a parancs eltávolítja a Group001 nevű erőforráscsoporthoz tartozó VMScaleSet001 nevű VMSS.</span><span class="sxs-lookup"><span data-stu-id="a6edd-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="a6edd-112">2. példa: virtuális gép eltávolítása egy VMSS belül</span><span class="sxs-lookup"><span data-stu-id="a6edd-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="a6edd-113">Ez a parancs eltávolítja a 3-as AZONOSÍTÓJÚ virtuális gépet a VMSS nevű VMScaleSet002, amely a Group002 nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="a6edd-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="a6edd-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6edd-114">PARAMETERS</span></span>

### <span data-ttu-id="a6edd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6edd-115">-AsJob</span></span>
<span data-ttu-id="a6edd-116">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="a6edd-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a6edd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6edd-117">-DefaultProfile</span></span>
<span data-ttu-id="a6edd-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6edd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6edd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a6edd-119">-Force</span></span>
<span data-ttu-id="a6edd-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a6edd-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a6edd-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a6edd-121">-InstanceId</span></span>
<span data-ttu-id="a6edd-122">Karakterláncként adja meg a kezdéshez szükséges példányok AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="a6edd-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="a6edd-123">Például: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="a6edd-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="a6edd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6edd-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6edd-125">Annak a csoportnak a neve, amelyhez a VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="a6edd-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="a6edd-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a6edd-126">-VMScaleSetName</span></span>
<span data-ttu-id="a6edd-127">Faj: a parancsmag által eltávolított VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="a6edd-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="a6edd-128">Ha a *InstanceId* paramétert adja meg, a parancsmag eltávolítja a megadott virtuális gépet a paraméter által megnevezett VMSS.</span><span class="sxs-lookup"><span data-stu-id="a6edd-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="a6edd-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a6edd-129">-Confirm</span></span>
<span data-ttu-id="a6edd-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a6edd-130">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6edd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6edd-131">-WhatIf</span></span>
<span data-ttu-id="a6edd-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a6edd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6edd-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6edd-133">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6edd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6edd-134">CommonParameters</span></span>
<span data-ttu-id="a6edd-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6edd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6edd-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6edd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6edd-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6edd-137">INPUTS</span></span>

### <span data-ttu-id="a6edd-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="a6edd-138">None</span></span>
<span data-ttu-id="a6edd-139">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a6edd-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6edd-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6edd-140">OUTPUTS</span></span>

### <span data-ttu-id="a6edd-141">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a6edd-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a6edd-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6edd-142">NOTES</span></span>

## <span data-ttu-id="a6edd-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6edd-143">RELATED LINKS</span></span>

[<span data-ttu-id="a6edd-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6edd-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="a6edd-145">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6edd-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="a6edd-146">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6edd-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="a6edd-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6edd-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="a6edd-148">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6edd-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="a6edd-149">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6edd-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="a6edd-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6edd-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


