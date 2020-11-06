---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVM.md
ms.openlocfilehash: 00325dc33daa6ec58693dbe6cd6d526ac41b8fd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502208"
---
# <span data-ttu-id="a1d69-101">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="a1d69-101">Get-AzureRmVmssVM</span></span>

## <span data-ttu-id="a1d69-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1d69-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d69-103">A VMSS virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a1d69-103">Gets the properties of a VMSS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1d69-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1d69-104">SYNTAX</span></span>

### <span data-ttu-id="a1d69-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1d69-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1d69-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="a1d69-106">FriendMethod</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1d69-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1d69-107">DESCRIPTION</span></span>
<span data-ttu-id="a1d69-108">A **Get-AzureRmVmssVM** parancsmag a Virtual Machine Scale set (VMSS) virtuális gép modell nézetét és példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a1d69-108">The **Get-AzureRmVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="a1d69-109">A modell nézet a virtuális gép felhasználó által megadott tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="a1d69-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="a1d69-110">A példány nézet a virtuális gép példány szintjének állapota.</span><span class="sxs-lookup"><span data-stu-id="a1d69-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="a1d69-111">Adja meg az *állapot* paramétert, hogy csak a virtuális gép példány nézete legyen látható.</span><span class="sxs-lookup"><span data-stu-id="a1d69-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="a1d69-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a1d69-112">EXAMPLES</span></span>

### <span data-ttu-id="a1d69-113">Példa 1: VMSS virtuális gép tulajdonságainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="a1d69-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="a1d69-114">Ez a parancs a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a1d69-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="a1d69-115">Mivel a parancs nem adja meg a *InstanceView* kapcsoló paramétert, a parancsmag a virtuális gép modell nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="a1d69-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="a1d69-116">2. példa: a VMSS virtuális gép modell nézetének tulajdonságainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="a1d69-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="a1d69-117">Ez a parancs a Group002 nevű erőforráscsoport VMSS004 tartozó VMSS virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a1d69-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="a1d69-118">A parancs a minta nézetet tartalmazó változóban tárolt példány AZONOSÍTÓját kapja meg $ID.</span><span class="sxs-lookup"><span data-stu-id="a1d69-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="a1d69-119">3. példa: VMSS virtuális gép példány nézetének tulajdonságainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="a1d69-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="a1d69-120">Ez a parancs a Group002 nevű erőforráscsoport VMSS004 tartozó VMSS virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a1d69-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="a1d69-121">Mivel a parancs a *InstanceView* kapcsoló paramétert adja meg, a parancsmag a virtuális gép példány nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="a1d69-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="a1d69-122">A parancs a példány nézethez tartozó változóban tárolt példány AZONOSÍTÓját kapja meg $ID.</span><span class="sxs-lookup"><span data-stu-id="a1d69-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="a1d69-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1d69-123">PARAMETERS</span></span>

### <span data-ttu-id="a1d69-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d69-124">-DefaultProfile</span></span>
<span data-ttu-id="a1d69-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1d69-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1d69-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a1d69-126">-InstanceId</span></span>
<span data-ttu-id="a1d69-127">Annak a példánynak az AZONOSÍTÓját adja meg, amelynek a modell nézetét be szeretné szerezni.</span><span class="sxs-lookup"><span data-stu-id="a1d69-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d69-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="a1d69-128">-InstanceView</span></span>
<span data-ttu-id="a1d69-129">Azt jelzi, hogy ez a parancsmag csak a virtuális gép példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a1d69-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="a1d69-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d69-130">-ResourceGroupName</span></span>
<span data-ttu-id="a1d69-131">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1d69-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="a1d69-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a1d69-132">-VMScaleSetName</span></span>
<span data-ttu-id="a1d69-133">Faj: a VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="a1d69-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="a1d69-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d69-134">CommonParameters</span></span>
<span data-ttu-id="a1d69-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1d69-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d69-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1d69-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d69-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1d69-137">INPUTS</span></span>

### <span data-ttu-id="a1d69-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a1d69-138">System.String</span></span>

## <span data-ttu-id="a1d69-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1d69-139">OUTPUTS</span></span>

### <span data-ttu-id="a1d69-140">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="a1d69-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="a1d69-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1d69-141">NOTES</span></span>

## <span data-ttu-id="a1d69-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1d69-142">RELATED LINKS</span></span>

[<span data-ttu-id="a1d69-143">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="a1d69-143">Set-AzureRmVmssVM</span></span>](./Set-AzureRmVmssVM.md)

[<span data-ttu-id="a1d69-144">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a1d69-144">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

