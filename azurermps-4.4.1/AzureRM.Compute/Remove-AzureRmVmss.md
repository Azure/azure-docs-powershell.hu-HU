---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 703fc0d83fb17e1131c44cbd06593887ebcce020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492537"
---
# <span data-ttu-id="97b78-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="97b78-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="97b78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97b78-102">SYNOPSIS</span></span>
<span data-ttu-id="97b78-103">Eltávolítja a VMSS belüli VMSS vagy virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="97b78-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97b78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97b78-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97b78-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97b78-105">DESCRIPTION</span></span>
<span data-ttu-id="97b78-106">A **Remove-AzureRmVmss** parancsmag eltávolítja a virtuális gép méretarányát (VMSS) az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="97b78-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="97b78-107">Ez a parancsmag a VMSS belül egy adott virtuális gép eltávolítására is használható.</span><span class="sxs-lookup"><span data-stu-id="97b78-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="97b78-108">A *InstanceId* paraméterrel eltávolíthatja egy adott virtuális GÉPET a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="97b78-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="97b78-109">Példák</span><span class="sxs-lookup"><span data-stu-id="97b78-109">EXAMPLES</span></span>

### <span data-ttu-id="97b78-110">1. példa: VMSS eltávolítása</span><span class="sxs-lookup"><span data-stu-id="97b78-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="97b78-111">Ez a parancs eltávolítja a Group001 nevű erőforráscsoporthoz tartozó VMScaleSet001 nevű VMSS.</span><span class="sxs-lookup"><span data-stu-id="97b78-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="97b78-112">2. példa: virtuális gép eltávolítása egy VMSS belül</span><span class="sxs-lookup"><span data-stu-id="97b78-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="97b78-113">Ez a parancs eltávolítja a 3-as AZONOSÍTÓJÚ virtuális gépet a VMSS nevű VMScaleSet002, amely a Group002 nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="97b78-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="97b78-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97b78-114">PARAMETERS</span></span>

### <span data-ttu-id="97b78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b78-115">-DefaultProfile</span></span>
<span data-ttu-id="97b78-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97b78-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97b78-117">-Force</span><span class="sxs-lookup"><span data-stu-id="97b78-117">-Force</span></span>
<span data-ttu-id="97b78-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="97b78-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97b78-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="97b78-119">-InstanceId</span></span>
<span data-ttu-id="97b78-120">Karakterláncként adja meg a kezdéshez szükséges példányok AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="97b78-120">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="97b78-121">Például: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="97b78-121">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="97b78-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b78-122">-ResourceGroupName</span></span>
<span data-ttu-id="97b78-123">Annak a csoportnak a neve, amelyhez a VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="97b78-123">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="97b78-124">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="97b78-124">-VMScaleSetName</span></span>
<span data-ttu-id="97b78-125">Faj: a parancsmag által eltávolított VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="97b78-125">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="97b78-126">Ha a *InstanceId* paramétert adja meg, a parancsmag eltávolítja a megadott virtuális gépet a paraméter által megnevezett VMSS.</span><span class="sxs-lookup"><span data-stu-id="97b78-126">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="97b78-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="97b78-127">-Confirm</span></span>
<span data-ttu-id="97b78-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97b78-128">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b78-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97b78-129">-WhatIf</span></span>
<span data-ttu-id="97b78-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="97b78-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97b78-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97b78-131">The cmdlet is not run.</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b78-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b78-132">CommonParameters</span></span>
<span data-ttu-id="97b78-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97b78-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b78-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b78-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b78-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97b78-135">INPUTS</span></span>

## <span data-ttu-id="97b78-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97b78-136">OUTPUTS</span></span>

## <span data-ttu-id="97b78-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97b78-137">NOTES</span></span>

## <span data-ttu-id="97b78-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97b78-138">RELATED LINKS</span></span>

[<span data-ttu-id="97b78-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="97b78-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="97b78-140">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="97b78-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="97b78-141">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="97b78-141">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="97b78-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="97b78-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="97b78-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="97b78-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="97b78-144">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="97b78-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="97b78-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="97b78-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


