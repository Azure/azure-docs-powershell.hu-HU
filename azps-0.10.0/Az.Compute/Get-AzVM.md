---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 2f33b0dbee4f584553eac1047471adef08e3523b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844634"
---
# <span data-ttu-id="f364d-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f364d-101">Get-AzVM</span></span>

## <span data-ttu-id="f364d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f364d-102">SYNOPSIS</span></span>
<span data-ttu-id="f364d-103">Egy virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f364d-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="f364d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f364d-104">SYNTAX</span></span>

### <span data-ttu-id="f364d-105">ListAllVirtualMachinesParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f364d-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f364d-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="f364d-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f364d-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="f364d-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f364d-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="f364d-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f364d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f364d-109">DESCRIPTION</span></span>
<span data-ttu-id="f364d-110">A **Get-AzVM** parancsmag az Azure Virtual Machine modell nézetét és példányának nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="f364d-110">The **Get-AzVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="f364d-111">A modell nézet a virtuális gép felhasználó által megadott tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="f364d-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="f364d-112">A példány nézet a virtuális gép példány szintjének állapota.</span><span class="sxs-lookup"><span data-stu-id="f364d-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="f364d-113">Adja meg az *állapot* paramétert, hogy csak a virtuális gép példány nézete legyen látható.</span><span class="sxs-lookup"><span data-stu-id="f364d-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="f364d-114">Példák</span><span class="sxs-lookup"><span data-stu-id="f364d-114">EXAMPLES</span></span>

### <span data-ttu-id="f364d-115">Példa 1: a modell és a példány nézet tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="f364d-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="f364d-116">Ez a parancs a VirtualMachine07 nevű virtuális gép modell nézetét és példány nézetének tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f364d-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="f364d-117">2. példa: a példány nézet tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="f364d-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="f364d-118">Ez a parancs a VirtualMachine07 nevű virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f364d-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="f364d-119">Ez a parancs az *állapot* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f364d-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="f364d-120">Így a parancs csak a példány nézet tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f364d-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="f364d-121">3. példa: tulajdonságok beolvasása az erőforráscsoport minden virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="f364d-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f364d-122">Ez a parancs a ResourceGroup11 nevű erőforráscsoport minden virtuális számítógépének tulajdonságait beolvassa.</span><span class="sxs-lookup"><span data-stu-id="f364d-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="f364d-123">Példa 4: az előfizetésben szereplő összes virtuális gép beszerzése</span><span class="sxs-lookup"><span data-stu-id="f364d-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM
```

<span data-ttu-id="f364d-124">Ez a parancs a virtuális gépeket az előfizetésében kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f364d-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="f364d-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f364d-125">PARAMETERS</span></span>

### <span data-ttu-id="f364d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f364d-126">-DefaultProfile</span></span>
<span data-ttu-id="f364d-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f364d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f364d-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="f364d-128">-DisplayHint</span></span>
<span data-ttu-id="f364d-129">A virtuálisgép-objektum megjelenési módjának meghatározása</span><span class="sxs-lookup"><span data-stu-id="f364d-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="f364d-130">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="f364d-130">Valid values are:</span></span>

<span data-ttu-id="f364d-131">– Tömörít: csak a legfelső szintű tulajdonságokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="f364d-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="f364d-132">– Kibontott: az összes tulajdonság megjelenítése minden szinten</span><span class="sxs-lookup"><span data-stu-id="f364d-132">-- Expand: displays all properties in all levels</span></span>
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: 
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f364d-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f364d-133">-Name</span></span>
<span data-ttu-id="f364d-134">A beolvasott virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f364d-134">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f364d-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="f364d-135">-NextLink</span></span>
<span data-ttu-id="f364d-136">A következő hivatkozást adja meg.</span><span class="sxs-lookup"><span data-stu-id="f364d-136">Specifies the next link.</span></span>

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f364d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f364d-137">-ResourceGroupName</span></span>
<span data-ttu-id="f364d-138">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f364d-138">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f364d-139">-Állapot</span><span class="sxs-lookup"><span data-stu-id="f364d-139">-Status</span></span>
<span data-ttu-id="f364d-140">Azt jelzi, hogy ez a parancsmag csak a virtuális gép példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f364d-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f364d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f364d-141">CommonParameters</span></span>
<span data-ttu-id="f364d-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f364d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f364d-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f364d-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f364d-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f364d-144">INPUTS</span></span>

### <span data-ttu-id="f364d-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="f364d-145">None</span></span>
<span data-ttu-id="f364d-146">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f364d-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f364d-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f364d-147">OUTPUTS</span></span>

### <span data-ttu-id="f364d-148">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f364d-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="f364d-149">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="f364d-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="f364d-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f364d-150">NOTES</span></span>

## <span data-ttu-id="f364d-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f364d-151">RELATED LINKS</span></span>

[<span data-ttu-id="f364d-152">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="f364d-152">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="f364d-153">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="f364d-153">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="f364d-154">Újraindítás – AzVM</span><span class="sxs-lookup"><span data-stu-id="f364d-154">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="f364d-155">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="f364d-155">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="f364d-156">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="f364d-156">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="f364d-157">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f364d-157">Update-AzVM</span></span>](./Update-AzVM.md)


