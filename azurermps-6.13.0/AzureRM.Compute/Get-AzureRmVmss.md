---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: d2e9ad0d83c573292996b65924ab7078368d328f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679617"
---
# <span data-ttu-id="dd84e-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dd84e-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="dd84e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd84e-102">SYNOPSIS</span></span>
<span data-ttu-id="dd84e-103">Beolvassa a VMSS tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="dd84e-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd84e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd84e-104">SYNTAX</span></span>

### <span data-ttu-id="dd84e-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd84e-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd84e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="dd84e-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd84e-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="dd84e-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd84e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd84e-108">DESCRIPTION</span></span>
<span data-ttu-id="dd84e-109">A **Get-AzureRmVmss** parancsmag a virtuálisgép-készlet (VMSS) modell-és példány nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="dd84e-109">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="dd84e-110">A modell nézet a virtuális gép méretarányának a felhasználó által megadott tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd84e-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="dd84e-111">A példány nézet a virtuális gép méretarányának a példány szintjének állapota.</span><span class="sxs-lookup"><span data-stu-id="dd84e-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="dd84e-112">Adja meg a *InstanceView* paramétert úgy, hogy csak a virtuálisgép-készlet példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dd84e-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="dd84e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="dd84e-113">EXAMPLES</span></span>

### <span data-ttu-id="dd84e-114">Példa 1: VMSS tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="dd84e-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="dd84e-115">Ez a parancs beolvassa a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="dd84e-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="dd84e-116">Mivel a parancs nem adja meg a *InstanceView* kapcsoló paramétert, a parancsmag a virtuális gép méretarányának modell nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dd84e-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

## <span data-ttu-id="dd84e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd84e-117">PARAMETERS</span></span>

### <span data-ttu-id="dd84e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd84e-118">-DefaultProfile</span></span>
<span data-ttu-id="dd84e-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd84e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd84e-120">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="dd84e-120">-InstanceView</span></span>
<span data-ttu-id="dd84e-121">Azt jelzi, hogy ez a parancsmag csak a virtuálisgép-készlet példányának nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dd84e-121">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="dd84e-122">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="dd84e-122">-OSUpgradeHistory</span></span>
<span data-ttu-id="dd84e-123">Azt jelzi, hogy ez a parancsmag a virtuális gép méretarányát tároló operációs rendszer frissítési előzményeit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="dd84e-123">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd84e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd84e-124">-ResourceGroupName</span></span>
<span data-ttu-id="dd84e-125">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd84e-125">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd84e-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="dd84e-126">-VMScaleSetName</span></span>
<span data-ttu-id="dd84e-127">Faj: a VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="dd84e-127">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd84e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd84e-128">CommonParameters</span></span>
<span data-ttu-id="dd84e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd84e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd84e-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd84e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd84e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd84e-131">INPUTS</span></span>

### <span data-ttu-id="dd84e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dd84e-132">System.String</span></span>

## <span data-ttu-id="dd84e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd84e-133">OUTPUTS</span></span>

### <span data-ttu-id="dd84e-134">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dd84e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="dd84e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd84e-135">NOTES</span></span>

## <span data-ttu-id="dd84e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd84e-136">RELATED LINKS</span></span>

[<span data-ttu-id="dd84e-137">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dd84e-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="dd84e-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dd84e-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="dd84e-139">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dd84e-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="dd84e-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dd84e-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="dd84e-141">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dd84e-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="dd84e-142">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dd84e-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="dd84e-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="dd84e-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


