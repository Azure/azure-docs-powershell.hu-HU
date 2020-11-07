---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
ms.openlocfilehash: d3706a7beb336dad870518ef9be0b26b41920007
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836811"
---
# <span data-ttu-id="9ced8-101">Disable-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="9ced8-101">Disable-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="9ced8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ced8-102">SYNOPSIS</span></span>
<span data-ttu-id="9ced8-103">Letiltja a lemez titkosítását a VM-léptékű készleteken.</span><span class="sxs-lookup"><span data-stu-id="9ced8-103">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="9ced8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ced8-104">SYNTAX</span></span>

```
Disable-AzVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ced8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ced8-105">DESCRIPTION</span></span>
<span data-ttu-id="9ced8-106">Letiltja a lemez titkosítását a VM-léptékű készleteken.</span><span class="sxs-lookup"><span data-stu-id="9ced8-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="9ced8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9ced8-107">EXAMPLES</span></span>

### <span data-ttu-id="9ced8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9ced8-108">Example 1</span></span>
```
PS C:\> Disable-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="9ced8-109">Letiltja a VMSS001 nevű, a Group001 nevű erőforráscsoport csoportjába tartozó "VM" méretarányt.</span><span class="sxs-lookup"><span data-stu-id="9ced8-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="9ced8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ced8-110">PARAMETERS</span></span>

### <span data-ttu-id="9ced8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ced8-111">-AsJob</span></span>
<span data-ttu-id="9ced8-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9ced8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ced8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ced8-113">-DefaultProfile</span></span>
<span data-ttu-id="9ced8-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ced8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ced8-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="9ced8-115">-ExtensionName</span></span>
<span data-ttu-id="9ced8-116">A kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="9ced8-116">The extension name.</span></span>
<span data-ttu-id="9ced8-117">Ha ez a paraméter nincs megadva, az alapértelmezett értékek a Windows VMs-AzureDiskEncryption és a Linux VMs-AzureDiskEncryptionForLinux használhatók.</span><span class="sxs-lookup"><span data-stu-id="9ced8-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ced8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9ced8-118">-Force</span></span>
<span data-ttu-id="9ced8-119">A kiterjesztés eltávolításának kényszerítése a virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="9ced8-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="9ced8-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="9ced8-120">-ForceUpdate</span></span>
<span data-ttu-id="9ced8-121">Címke létrehozása a haderő frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="9ced8-121">Generate a tag for force update.</span></span>  <span data-ttu-id="9ced8-122">Ezt meg kell adni az ismétlődő titkosítási műveletek elvégzésének ugyanazon a VM-eszközön.</span><span class="sxs-lookup"><span data-stu-id="9ced8-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ced8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ced8-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ced8-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9ced8-124">The resource group name.</span></span>

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

### <span data-ttu-id="9ced8-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9ced8-125">-VMScaleSetName</span></span>
<span data-ttu-id="9ced8-126">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="9ced8-126">The virtual machine name.</span></span>

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

### <span data-ttu-id="9ced8-127">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="9ced8-127">-VolumeType</span></span>
<span data-ttu-id="9ced8-128">A titkosítási művelet elvégzéséhez használt hangerő (operációs rendszer vagy adat) típusa</span><span class="sxs-lookup"><span data-stu-id="9ced8-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ced8-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9ced8-129">-Confirm</span></span>
<span data-ttu-id="9ced8-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9ced8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ced8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ced8-131">-WhatIf</span></span>
<span data-ttu-id="9ced8-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9ced8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ced8-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ced8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ced8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ced8-134">CommonParameters</span></span>
<span data-ttu-id="9ced8-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ced8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ced8-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ced8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ced8-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ced8-137">INPUTS</span></span>

### <span data-ttu-id="9ced8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9ced8-138">System.String</span></span>

### <span data-ttu-id="9ced8-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9ced8-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9ced8-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ced8-140">OUTPUTS</span></span>

### <span data-ttu-id="9ced8-141">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9ced8-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="9ced8-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ced8-142">NOTES</span></span>

## <span data-ttu-id="9ced8-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ced8-143">RELATED LINKS</span></span>
