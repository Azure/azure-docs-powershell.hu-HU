---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: efb24aa4f8770e1911b9bf85a1fbf4dd366ea34d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492500"
---
# <span data-ttu-id="13b99-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13b99-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="13b99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13b99-102">SYNOPSIS</span></span>
<span data-ttu-id="13b99-103">Meghatározott műveleteket határoz meg a megadott VMSS.</span><span class="sxs-lookup"><span data-stu-id="13b99-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13b99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13b99-104">SYNTAX</span></span>

### <span data-ttu-id="13b99-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13b99-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13b99-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="13b99-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13b99-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="13b99-107">DESCRIPTION</span></span>
<span data-ttu-id="13b99-108">A **set-AzureRmVmss** parancsmag meghatározott műveleteket állít be a virtuálisgép-készlet (VMSS) beállításnál.</span><span class="sxs-lookup"><span data-stu-id="13b99-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="13b99-109">A csak a parancsmag által támogatott műveletek a Reimage.</span><span class="sxs-lookup"><span data-stu-id="13b99-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="13b99-110">Példák</span><span class="sxs-lookup"><span data-stu-id="13b99-110">EXAMPLES</span></span>

### <span data-ttu-id="13b99-111">Példa 1: VMSS</span><span class="sxs-lookup"><span data-stu-id="13b99-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="13b99-112">Ez a parancs a ContosoGroup nevű erőforráscsoporthoz tartozó ContosoVMSS VMSS.</span><span class="sxs-lookup"><span data-stu-id="13b99-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="13b99-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13b99-113">PARAMETERS</span></span>

### <span data-ttu-id="13b99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b99-114">-DefaultProfile</span></span>
<span data-ttu-id="13b99-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13b99-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13b99-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="13b99-116">-InstanceId</span></span>
<span data-ttu-id="13b99-117">A virtuális gép példányának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="13b99-117">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="13b99-118">-Reimage</span><span class="sxs-lookup"><span data-stu-id="13b99-118">-Reimage</span></span>
<span data-ttu-id="13b99-119">Jelzi, hogy a parancsmag átadja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="13b99-119">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b99-120">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="13b99-120">-ReimageAll</span></span>
<span data-ttu-id="13b99-121">Jelzi, hogy a parancsmag a VMSS összes lemezét átadja.</span><span class="sxs-lookup"><span data-stu-id="13b99-121">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b99-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13b99-122">-ResourceGroupName</span></span>
<span data-ttu-id="13b99-123">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13b99-123">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="13b99-124">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="13b99-124">-VMScaleSetName</span></span>
<span data-ttu-id="13b99-125">Faj: annak a VMSS a neve, amelyhez a parancsmag a műveleteket állítja be.</span><span class="sxs-lookup"><span data-stu-id="13b99-125">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="13b99-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13b99-126">-Confirm</span></span>
<span data-ttu-id="13b99-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13b99-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13b99-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13b99-128">-WhatIf</span></span>
<span data-ttu-id="13b99-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13b99-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13b99-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13b99-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13b99-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b99-131">CommonParameters</span></span>
<span data-ttu-id="13b99-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13b99-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b99-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13b99-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b99-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13b99-134">INPUTS</span></span>

## <span data-ttu-id="13b99-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13b99-135">OUTPUTS</span></span>

### <span data-ttu-id="13b99-136">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="13b99-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="13b99-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13b99-137">NOTES</span></span>

## <span data-ttu-id="13b99-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13b99-138">RELATED LINKS</span></span>

[<span data-ttu-id="13b99-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13b99-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="13b99-140">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13b99-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="13b99-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13b99-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="13b99-142">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13b99-142">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="13b99-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13b99-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="13b99-144">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13b99-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="13b99-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13b99-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


