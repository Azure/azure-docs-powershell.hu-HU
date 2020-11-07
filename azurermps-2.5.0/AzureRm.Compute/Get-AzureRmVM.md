---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
ms.openlocfilehash: 832a7c81c9c7e8ffa5a5a6123162746d039ca71d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848905"
---
# <span data-ttu-id="aae0f-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aae0f-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="aae0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aae0f-102">SYNOPSIS</span></span>
<span data-ttu-id="aae0f-103">Egy virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aae0f-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aae0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aae0f-104">SYNTAX</span></span>

### <span data-ttu-id="aae0f-105">ListAllVirtualMachinesParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aae0f-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aae0f-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="aae0f-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aae0f-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="aae0f-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aae0f-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="aae0f-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aae0f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="aae0f-109">DESCRIPTION</span></span>
<span data-ttu-id="aae0f-110">A **Get-AzureRmVM** parancsmag az Azure Virtual Machine modell nézetét és példányának nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="aae0f-110">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="aae0f-111">A modell nézet a virtuális gép felhasználó által megadott tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="aae0f-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="aae0f-112">A példány nézet a virtuális gép példány szintjének állapota.</span><span class="sxs-lookup"><span data-stu-id="aae0f-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="aae0f-113">Adja meg az *állapot* paramétert, hogy csak a virtuális gép példány nézete legyen látható.</span><span class="sxs-lookup"><span data-stu-id="aae0f-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="aae0f-114">Példák</span><span class="sxs-lookup"><span data-stu-id="aae0f-114">EXAMPLES</span></span>

### <span data-ttu-id="aae0f-115">Példa 1: a modell és a példány nézet tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="aae0f-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="aae0f-116">Ez a parancs a VirtualMachine07 nevű virtuális gép modell nézetét és példány nézetének tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aae0f-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="aae0f-117">2. példa: a példány nézet tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="aae0f-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="aae0f-118">Ez a parancs a VirtualMachine07 nevű virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aae0f-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="aae0f-119">Ez a parancs az *állapot* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="aae0f-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="aae0f-120">Így a parancs csak a példány nézet tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aae0f-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="aae0f-121">3. példa: tulajdonságok beolvasása az erőforráscsoport minden virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="aae0f-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="aae0f-122">Ez a parancs a ResourceGroup11 nevű erőforráscsoport minden virtuális számítógépének tulajdonságait beolvassa.</span><span class="sxs-lookup"><span data-stu-id="aae0f-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="aae0f-123">Példa 4: az előfizetésben szereplő összes virtuális gép beszerzése</span><span class="sxs-lookup"><span data-stu-id="aae0f-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="aae0f-124">Ez a parancs a virtuális gépeket az előfizetésében kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aae0f-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="aae0f-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aae0f-125">PARAMETERS</span></span>

### <span data-ttu-id="aae0f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae0f-126">-DefaultProfile</span></span>
<span data-ttu-id="aae0f-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aae0f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aae0f-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="aae0f-128">-DisplayHint</span></span>
<span data-ttu-id="aae0f-129">A virtuálisgép-objektum megjelenési módjának meghatározása</span><span class="sxs-lookup"><span data-stu-id="aae0f-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="aae0f-130">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="aae0f-130">Valid values are:</span></span>

<span data-ttu-id="aae0f-131">– Tömörít: csak a legfelső szintű tulajdonságokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="aae0f-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="aae0f-132">– Kibontott: az összes tulajdonság megjelenítése minden szinten</span><span class="sxs-lookup"><span data-stu-id="aae0f-132">-- Expand: displays all properties in all levels</span></span>
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

### <span data-ttu-id="aae0f-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aae0f-133">-Name</span></span>
<span data-ttu-id="aae0f-134">A beolvasott virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aae0f-134">Specifies the name of the virtual machine to get.</span></span>

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

### <span data-ttu-id="aae0f-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="aae0f-135">-NextLink</span></span>
<span data-ttu-id="aae0f-136">A következő hivatkozást adja meg.</span><span class="sxs-lookup"><span data-stu-id="aae0f-136">Specifies the next link.</span></span>

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

### <span data-ttu-id="aae0f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aae0f-137">-ResourceGroupName</span></span>
<span data-ttu-id="aae0f-138">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aae0f-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="aae0f-139">-Állapot</span><span class="sxs-lookup"><span data-stu-id="aae0f-139">-Status</span></span>
<span data-ttu-id="aae0f-140">Azt jelzi, hogy ez a parancsmag csak a virtuális gép példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aae0f-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="aae0f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae0f-141">CommonParameters</span></span>
<span data-ttu-id="aae0f-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aae0f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae0f-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aae0f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae0f-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aae0f-144">INPUTS</span></span>

### <span data-ttu-id="aae0f-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="aae0f-145">None</span></span>
<span data-ttu-id="aae0f-146">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="aae0f-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aae0f-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aae0f-147">OUTPUTS</span></span>

### <span data-ttu-id="aae0f-148">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="aae0f-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="aae0f-149">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="aae0f-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="aae0f-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aae0f-150">NOTES</span></span>

## <span data-ttu-id="aae0f-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aae0f-151">RELATED LINKS</span></span>

[<span data-ttu-id="aae0f-152">Új – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aae0f-152">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="aae0f-153">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aae0f-153">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="aae0f-154">Újraindítás – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aae0f-154">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="aae0f-155">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aae0f-155">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="aae0f-156">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aae0f-156">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="aae0f-157">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aae0f-157">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


