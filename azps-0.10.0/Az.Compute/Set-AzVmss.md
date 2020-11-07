---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 5ceb420f30525817ebccd6d3f38a53e6c1cad66e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844178"
---
# <span data-ttu-id="a1bf5-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1bf5-101">Set-AzVmss</span></span>

## <span data-ttu-id="a1bf5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="a1bf5-103">Meghatározott műveleteket határoz meg a megadott VMSS.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="a1bf5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1bf5-104">SYNTAX</span></span>

### <span data-ttu-id="a1bf5-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1bf5-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1bf5-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="a1bf5-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1bf5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1bf5-107">DESCRIPTION</span></span>
<span data-ttu-id="a1bf5-108">A **set-AzVmss** parancsmag meghatározott műveleteket állít be a virtuálisgép-készlet (VMSS) beállításnál.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-108">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="a1bf5-109">A csak a parancsmag által támogatott műveletek a Reimage.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="a1bf5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a1bf5-110">EXAMPLES</span></span>

### <span data-ttu-id="a1bf5-111">Példa 1: VMSS</span><span class="sxs-lookup"><span data-stu-id="a1bf5-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="a1bf5-112">Ez a parancs a ContosoGroup nevű erőforráscsoporthoz tartozó ContosoVMSS VMSS.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="a1bf5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1bf5-113">PARAMETERS</span></span>

### <span data-ttu-id="a1bf5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1bf5-114">-AsJob</span></span>
<span data-ttu-id="a1bf5-115">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a1bf5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1bf5-116">-DefaultProfile</span></span>
<span data-ttu-id="a1bf5-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1bf5-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a1bf5-118">-InstanceId</span></span>
<span data-ttu-id="a1bf5-119">A virtuális gép példányának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-119">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="a1bf5-120">-Reimage</span><span class="sxs-lookup"><span data-stu-id="a1bf5-120">-Reimage</span></span>
<span data-ttu-id="a1bf5-121">Jelzi, hogy a parancsmag átadja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-121">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="a1bf5-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="a1bf5-122">-ReimageAll</span></span>
<span data-ttu-id="a1bf5-123">Jelzi, hogy a parancsmag a VMSS összes lemezét átadja.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="a1bf5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1bf5-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1bf5-125">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="a1bf5-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a1bf5-126">-VMScaleSetName</span></span>
<span data-ttu-id="a1bf5-127">Faj: annak a VMSS a neve, amelyhez a parancsmag a műveleteket állítja be.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="a1bf5-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a1bf5-128">-Confirm</span></span>
<span data-ttu-id="a1bf5-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1bf5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1bf5-130">-WhatIf</span></span>
<span data-ttu-id="a1bf5-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1bf5-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1bf5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1bf5-133">CommonParameters</span></span>
<span data-ttu-id="a1bf5-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1bf5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1bf5-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1bf5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1bf5-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1bf5-136">INPUTS</span></span>

### <span data-ttu-id="a1bf5-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="a1bf5-137">None</span></span>
<span data-ttu-id="a1bf5-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a1bf5-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1bf5-139">OUTPUTS</span></span>

### <span data-ttu-id="a1bf5-140">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a1bf5-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a1bf5-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1bf5-141">NOTES</span></span>

## <span data-ttu-id="a1bf5-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1bf5-142">RELATED LINKS</span></span>

[<span data-ttu-id="a1bf5-143">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1bf5-143">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="a1bf5-144">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1bf5-144">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="a1bf5-145">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1bf5-145">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="a1bf5-146">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1bf5-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="a1bf5-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1bf5-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="a1bf5-148">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1bf5-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="a1bf5-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a1bf5-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


