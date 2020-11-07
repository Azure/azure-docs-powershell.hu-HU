---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2d33f111928d0b022c7836d0b5c86fb5ec6f203e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849366"
---
# <span data-ttu-id="cf97e-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf97e-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="cf97e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf97e-102">SYNOPSIS</span></span>
<span data-ttu-id="cf97e-103">Meghatározott műveleteket határoz meg a megadott VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf97e-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf97e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf97e-104">SYNTAX</span></span>

### <span data-ttu-id="cf97e-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf97e-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf97e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="cf97e-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf97e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf97e-107">DESCRIPTION</span></span>
<span data-ttu-id="cf97e-108">A **set-AzureRmVmss** parancsmag meghatározott műveleteket állít be a virtuálisgép-készlet (VMSS) beállításnál.</span><span class="sxs-lookup"><span data-stu-id="cf97e-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="cf97e-109">A csak a parancsmag által támogatott műveletek a Reimage.</span><span class="sxs-lookup"><span data-stu-id="cf97e-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="cf97e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cf97e-110">EXAMPLES</span></span>

### <span data-ttu-id="cf97e-111">Példa 1: VMSS</span><span class="sxs-lookup"><span data-stu-id="cf97e-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="cf97e-112">Ez a parancs a ContosoGroup nevű erőforráscsoporthoz tartozó ContosoVMSS VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf97e-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="cf97e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf97e-113">PARAMETERS</span></span>

### <span data-ttu-id="cf97e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf97e-114">-AsJob</span></span>
<span data-ttu-id="cf97e-115">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="cf97e-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cf97e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf97e-116">-DefaultProfile</span></span>
<span data-ttu-id="cf97e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf97e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf97e-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="cf97e-118">-InstanceId</span></span>
<span data-ttu-id="cf97e-119">A virtuális gép példányának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cf97e-119">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="cf97e-120">-Reimage</span><span class="sxs-lookup"><span data-stu-id="cf97e-120">-Reimage</span></span>
<span data-ttu-id="cf97e-121">Jelzi, hogy a parancsmag átadja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf97e-121">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf97e-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="cf97e-122">-ReimageAll</span></span>
<span data-ttu-id="cf97e-123">Jelzi, hogy a parancsmag a VMSS összes lemezét átadja.</span><span class="sxs-lookup"><span data-stu-id="cf97e-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="cf97e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf97e-124">-ResourceGroupName</span></span>
<span data-ttu-id="cf97e-125">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf97e-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="cf97e-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cf97e-126">-VMScaleSetName</span></span>
<span data-ttu-id="cf97e-127">Faj: annak a VMSS a neve, amelyhez a parancsmag a műveleteket állítja be.</span><span class="sxs-lookup"><span data-stu-id="cf97e-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="cf97e-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf97e-128">-Confirm</span></span>
<span data-ttu-id="cf97e-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf97e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf97e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf97e-130">-WhatIf</span></span>
<span data-ttu-id="cf97e-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf97e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf97e-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf97e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf97e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf97e-133">CommonParameters</span></span>
<span data-ttu-id="cf97e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf97e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf97e-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf97e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf97e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf97e-136">INPUTS</span></span>

### <span data-ttu-id="cf97e-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="cf97e-137">None</span></span>
<span data-ttu-id="cf97e-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cf97e-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cf97e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf97e-139">OUTPUTS</span></span>

### <span data-ttu-id="cf97e-140">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cf97e-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="cf97e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf97e-141">NOTES</span></span>

## <span data-ttu-id="cf97e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf97e-142">RELATED LINKS</span></span>

[<span data-ttu-id="cf97e-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf97e-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="cf97e-144">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf97e-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="cf97e-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf97e-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="cf97e-146">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf97e-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="cf97e-147">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf97e-147">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="cf97e-148">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf97e-148">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="cf97e-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf97e-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


