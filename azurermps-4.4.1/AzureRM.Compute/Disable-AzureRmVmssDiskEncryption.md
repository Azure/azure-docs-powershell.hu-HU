---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 8cb68b45637496cb87e387c6755fe861fe3e21f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505195"
---
# <span data-ttu-id="5283a-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="5283a-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="5283a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5283a-102">SYNOPSIS</span></span>
<span data-ttu-id="5283a-103">Letiltja a lemez titkosítását a VM-léptékű készleteken.</span><span class="sxs-lookup"><span data-stu-id="5283a-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5283a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5283a-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5283a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5283a-105">DESCRIPTION</span></span>
<span data-ttu-id="5283a-106">Letiltja a lemez titkosítását a VM-léptékű készleteken.</span><span class="sxs-lookup"><span data-stu-id="5283a-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="5283a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5283a-107">EXAMPLES</span></span>

### <span data-ttu-id="5283a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5283a-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="5283a-109">Letiltja a VMSS001 nevű, a Group001 nevű erőforráscsoport csoportjába tartozó "VM" méretarányt.</span><span class="sxs-lookup"><span data-stu-id="5283a-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="5283a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5283a-110">PARAMETERS</span></span>

### <span data-ttu-id="5283a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5283a-111">-DefaultProfile</span></span>
<span data-ttu-id="5283a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5283a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5283a-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="5283a-113">-ExtensionName</span></span>
<span data-ttu-id="5283a-114">A kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="5283a-114">The extension name.</span></span>
<span data-ttu-id="5283a-115">Ha ez a paraméter nincs megadva, az alapértelmezett értékek a Windows VMs-AzureDiskEncryption és a Linux VMs-AzureDiskEncryptionForLinux használhatók.</span><span class="sxs-lookup"><span data-stu-id="5283a-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="5283a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5283a-116">-Force</span></span>
<span data-ttu-id="5283a-117">A kiterjesztés eltávolításának kényszerítése a virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="5283a-117">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="5283a-118">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="5283a-118">-ForceUpdate</span></span>
<span data-ttu-id="5283a-119">Címke létrehozása a haderő frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="5283a-119">Generate a tag for force update.</span></span>  <span data-ttu-id="5283a-120">Ezt meg kell adni az ismétlődő titkosítási műveletek elvégzésének ugyanazon a VM-eszközön.</span><span class="sxs-lookup"><span data-stu-id="5283a-120">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="5283a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5283a-121">-ResourceGroupName</span></span>
<span data-ttu-id="5283a-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="5283a-122">The resource group name.</span></span>

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

### <span data-ttu-id="5283a-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5283a-123">-VMScaleSetName</span></span>
<span data-ttu-id="5283a-124">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="5283a-124">The virtual machine name.</span></span>

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

### <span data-ttu-id="5283a-125">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="5283a-125">-VolumeType</span></span>
<span data-ttu-id="5283a-126">A titkosítási művelet elvégzéséhez használt hangerő (operációs rendszer vagy adat) típusa</span><span class="sxs-lookup"><span data-stu-id="5283a-126">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="5283a-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5283a-127">-Confirm</span></span>
<span data-ttu-id="5283a-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5283a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5283a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5283a-129">-WhatIf</span></span>
<span data-ttu-id="5283a-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5283a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5283a-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5283a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5283a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5283a-132">CommonParameters</span></span>
<span data-ttu-id="5283a-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5283a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5283a-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5283a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5283a-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5283a-135">INPUTS</span></span>

### <span data-ttu-id="5283a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5283a-136">System.String</span></span>

## <span data-ttu-id="5283a-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5283a-137">OUTPUTS</span></span>

### <span data-ttu-id="5283a-138">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5283a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5283a-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5283a-139">NOTES</span></span>

## <span data-ttu-id="5283a-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5283a-140">RELATED LINKS</span></span>

