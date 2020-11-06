---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
ms.openlocfilehash: fcde9de2862590cbf05d680c130bbf7b7f3070d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492560"
---
# <span data-ttu-id="312ab-101">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="312ab-101">Get-AzureRmVmssVM</span></span>

## <span data-ttu-id="312ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="312ab-102">SYNOPSIS</span></span>
<span data-ttu-id="312ab-103">A VMSS virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="312ab-103">Gets the properties of a VMSS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="312ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="312ab-104">SYNTAX</span></span>

### <span data-ttu-id="312ab-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="312ab-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="312ab-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="312ab-106">FriendMethod</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="312ab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="312ab-107">DESCRIPTION</span></span>
<span data-ttu-id="312ab-108">A **Get-AzureRmVmssVM** parancsmag a Virtual Machine Scale set (VMSS) virtuális gép modell nézetét és példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="312ab-108">The **Get-AzureRmVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="312ab-109">A modell nézet a virtuális gép felhasználó által megadott tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="312ab-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="312ab-110">A példány nézet a virtuális gép példány szintjének állapota.</span><span class="sxs-lookup"><span data-stu-id="312ab-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="312ab-111">Adja meg az *állapot* paramétert, hogy csak a virtuális gép példány nézete legyen látható.</span><span class="sxs-lookup"><span data-stu-id="312ab-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="312ab-112">Példák</span><span class="sxs-lookup"><span data-stu-id="312ab-112">EXAMPLES</span></span>

### <span data-ttu-id="312ab-113">Példa 1: VMSS virtuális gép tulajdonságainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="312ab-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="312ab-114">Ez a parancs a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="312ab-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="312ab-115">Mivel a parancs nem adja meg a *InstanceView* kapcsoló paramétert, a parancsmag a virtuális gép modell nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="312ab-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="312ab-116">2. példa: a VMSS virtuális gép modell nézetének tulajdonságainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="312ab-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="312ab-117">Ez a parancs a Group002 nevű erőforráscsoport VMSS004 tartozó VMSS virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="312ab-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="312ab-118">A parancs a minta nézetet tartalmazó változóban tárolt példány AZONOSÍTÓját kapja meg $ID.</span><span class="sxs-lookup"><span data-stu-id="312ab-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="312ab-119">3. példa: VMSS virtuális gép példány nézetének tulajdonságainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="312ab-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="312ab-120">Ez a parancs a Group002 nevű erőforráscsoport VMSS004 tartozó VMSS virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="312ab-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="312ab-121">Mivel a parancs a *InstanceView* kapcsoló paramétert adja meg, a parancsmag a virtuális gép példány nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="312ab-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="312ab-122">A parancs a példány nézethez tartozó változóban tárolt példány AZONOSÍTÓját kapja meg $ID.</span><span class="sxs-lookup"><span data-stu-id="312ab-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="312ab-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="312ab-123">PARAMETERS</span></span>

### <span data-ttu-id="312ab-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="312ab-124">-DefaultProfile</span></span>
<span data-ttu-id="312ab-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="312ab-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="312ab-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="312ab-126">-InstanceId</span></span>
<span data-ttu-id="312ab-127">Annak a példánynak az AZONOSÍTÓját adja meg, amelynek a modell nézetét be szeretné szerezni.</span><span class="sxs-lookup"><span data-stu-id="312ab-127">Specifies the instance ID for which to get the model view.</span></span>

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

### <span data-ttu-id="312ab-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="312ab-128">-InstanceView</span></span>
<span data-ttu-id="312ab-129">Azt jelzi, hogy ez a parancsmag csak a virtuális gép példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="312ab-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="312ab-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="312ab-130">-ResourceGroupName</span></span>
<span data-ttu-id="312ab-131">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="312ab-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="312ab-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="312ab-132">-VMScaleSetName</span></span>
<span data-ttu-id="312ab-133">Faj: a VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="312ab-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="312ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="312ab-134">CommonParameters</span></span>
<span data-ttu-id="312ab-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="312ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="312ab-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="312ab-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="312ab-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="312ab-137">INPUTS</span></span>

## <span data-ttu-id="312ab-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="312ab-138">OUTPUTS</span></span>

### <span data-ttu-id="312ab-139">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="312ab-139">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="312ab-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="312ab-140">NOTES</span></span>

## <span data-ttu-id="312ab-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="312ab-141">RELATED LINKS</span></span>

[<span data-ttu-id="312ab-142">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="312ab-142">Set-AzureRmVmssVM</span></span>](./Set-AzureRmVmssVM.md)

[<span data-ttu-id="312ab-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="312ab-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


