---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: 61bd867f7790f47599ac10ebd6523327e4e1868a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671262"
---
# <span data-ttu-id="d10d2-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d10d2-101">Restart-AzVmss</span></span>

## <span data-ttu-id="d10d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d10d2-102">SYNOPSIS</span></span>
<span data-ttu-id="d10d2-103">A VMSS vagy egy virtuális gép újraindítása a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="d10d2-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="d10d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d10d2-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d10d2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d10d2-105">DESCRIPTION</span></span>
<span data-ttu-id="d10d2-106">Az **Újraindítás-AzVmss** parancsmag újraindítja a virtuálisgép-készletet (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d10d2-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="d10d2-107">Ez a parancsmag azt is megteheti, hogy a *InstanceId* paraméterrel az adott virtuális gép újraindítása a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="d10d2-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="d10d2-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d10d2-108">EXAMPLES</span></span>

### <span data-ttu-id="d10d2-109">Példa 1: a VMSS újraindítása</span><span class="sxs-lookup"><span data-stu-id="d10d2-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="d10d2-110">Ez a parancs elindítja a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS.</span><span class="sxs-lookup"><span data-stu-id="d10d2-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="d10d2-111">2. példa: egy adott virtuális gép újraindítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="d10d2-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="d10d2-112">Ez a parancs egy olyan virtuális gépet indít elő, amely az 1-es azonosítójú példány azonosítóját tartalmazza a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS.</span><span class="sxs-lookup"><span data-stu-id="d10d2-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="d10d2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d10d2-113">PARAMETERS</span></span>

### <span data-ttu-id="d10d2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d10d2-114">-AsJob</span></span>
<span data-ttu-id="d10d2-115">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="d10d2-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d10d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d10d2-116">-DefaultProfile</span></span>
<span data-ttu-id="d10d2-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d10d2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d10d2-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d10d2-118">-InstanceId</span></span>
<span data-ttu-id="d10d2-119">Karakterláncként adja meg az újraindítani kívánt példányok AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="d10d2-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d10d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d10d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="d10d2-121">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d10d2-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="d10d2-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d10d2-122">-VMScaleSetName</span></span>
<span data-ttu-id="d10d2-123">Faj: annak a VMSS a neve, amelyre a parancsmag újraindult.</span><span class="sxs-lookup"><span data-stu-id="d10d2-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="d10d2-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d10d2-124">-Confirm</span></span>
<span data-ttu-id="d10d2-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d10d2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d10d2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d10d2-126">-WhatIf</span></span>
<span data-ttu-id="d10d2-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d10d2-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d10d2-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d10d2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d10d2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d10d2-129">CommonParameters</span></span>
<span data-ttu-id="d10d2-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d10d2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d10d2-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d10d2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d10d2-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d10d2-132">INPUTS</span></span>

### <span data-ttu-id="d10d2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d10d2-133">System.String</span></span>

### <span data-ttu-id="d10d2-134">System. string []</span><span class="sxs-lookup"><span data-stu-id="d10d2-134">System.String[]</span></span>

## <span data-ttu-id="d10d2-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d10d2-135">OUTPUTS</span></span>

### <span data-ttu-id="d10d2-136">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d10d2-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d10d2-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d10d2-137">NOTES</span></span>

## <span data-ttu-id="d10d2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d10d2-138">RELATED LINKS</span></span>

[<span data-ttu-id="d10d2-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d10d2-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="d10d2-140">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="d10d2-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="d10d2-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d10d2-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="d10d2-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d10d2-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="d10d2-143">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d10d2-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="d10d2-144">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d10d2-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="d10d2-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d10d2-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


