---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: 8601a7cc6a02211a0264030784485a5ecb4d29fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494131"
---
# <span data-ttu-id="13ec5-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="13ec5-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="13ec5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="13ec5-103">Egy virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="13ec5-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13ec5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13ec5-104">SYNTAX</span></span>

### <span data-ttu-id="13ec5-105">ListAllVirtualMachinesParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13ec5-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13ec5-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="13ec5-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13ec5-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="13ec5-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13ec5-108">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="13ec5-108">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13ec5-109">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="13ec5-109">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13ec5-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="13ec5-110">DESCRIPTION</span></span>
<span data-ttu-id="13ec5-111">A **Get-AzureRmVM** parancsmag az Azure Virtual Machine modell nézetét és példányának nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="13ec5-111">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="13ec5-112">A modell nézet a virtuális gép felhasználó által megadott tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="13ec5-112">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="13ec5-113">A példány nézet a virtuális gép példány szintjének állapota.</span><span class="sxs-lookup"><span data-stu-id="13ec5-113">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="13ec5-114">Adja meg az *állapot* paramétert, hogy csak a virtuális gép példány nézete legyen látható.</span><span class="sxs-lookup"><span data-stu-id="13ec5-114">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="13ec5-115">Példák</span><span class="sxs-lookup"><span data-stu-id="13ec5-115">EXAMPLES</span></span>

### <span data-ttu-id="13ec5-116">Példa 1: a modell és a példány nézet tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="13ec5-116">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="13ec5-117">Ez a parancs a VirtualMachine07 nevű virtuális gép modell nézetét és példány nézetének tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="13ec5-117">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="13ec5-118">2. példa: a példány nézet tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="13ec5-118">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="13ec5-119">Ez a parancs a VirtualMachine07 nevű virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="13ec5-119">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="13ec5-120">Ez a parancs az *állapot* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="13ec5-120">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="13ec5-121">Így a parancs csak a példány nézet tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="13ec5-121">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="13ec5-122">3. példa: tulajdonságok beolvasása az erőforráscsoport minden virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="13ec5-122">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="13ec5-123">Ez a parancs a ResourceGroup11 nevű erőforráscsoport minden virtuális számítógépének tulajdonságait beolvassa.</span><span class="sxs-lookup"><span data-stu-id="13ec5-123">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="13ec5-124">Példa 4: az előfizetésben szereplő összes virtuális gép beszerzése</span><span class="sxs-lookup"><span data-stu-id="13ec5-124">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="13ec5-125">Ez a parancs a virtuális gépeket az előfizetésében kapja meg.</span><span class="sxs-lookup"><span data-stu-id="13ec5-125">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="13ec5-126">Példa 5: az összes virtuális gép lekérése a helyről.</span><span class="sxs-lookup"><span data-stu-id="13ec5-126">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzureRmVM -Location "westus"
```

<span data-ttu-id="13ec5-127">Ez a parancs a Nyugat-amerikai régió minden virtuális számítógépét bekapja.</span><span class="sxs-lookup"><span data-stu-id="13ec5-127">This command gets all the virtual machines in West US region.</span></span>

## <span data-ttu-id="13ec5-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13ec5-128">PARAMETERS</span></span>

### <span data-ttu-id="13ec5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ec5-129">-DefaultProfile</span></span>
<span data-ttu-id="13ec5-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13ec5-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13ec5-131">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="13ec5-131">-DisplayHint</span></span>
<span data-ttu-id="13ec5-132">A virtuálisgép-objektum megjelenési módjának meghatározása</span><span class="sxs-lookup"><span data-stu-id="13ec5-132">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="13ec5-133">Az érvényes értékek:--kompakt: csak a legfelső szintű tulajdonságokat jeleníti meg – a Kibontás: az összes tulajdonság megjelenítése minden szinten.</span><span class="sxs-lookup"><span data-stu-id="13ec5-133">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13ec5-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="13ec5-134">-Location</span></span>
<span data-ttu-id="13ec5-135">A lista virtuális gépei helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13ec5-135">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13ec5-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13ec5-136">-Name</span></span>
<span data-ttu-id="13ec5-137">A beolvasott virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13ec5-137">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13ec5-138">-NextLink</span><span class="sxs-lookup"><span data-stu-id="13ec5-138">-NextLink</span></span>
<span data-ttu-id="13ec5-139">A következő hivatkozást adja meg.</span><span class="sxs-lookup"><span data-stu-id="13ec5-139">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13ec5-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ec5-140">-ResourceGroupName</span></span>
<span data-ttu-id="13ec5-141">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13ec5-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13ec5-142">-Állapot</span><span class="sxs-lookup"><span data-stu-id="13ec5-142">-Status</span></span>
<span data-ttu-id="13ec5-143">Azt jelzi, hogy ez a parancsmag csak a virtuális gép példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="13ec5-143">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ec5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ec5-144">CommonParameters</span></span>
<span data-ttu-id="13ec5-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13ec5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ec5-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13ec5-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ec5-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13ec5-147">INPUTS</span></span>

### <span data-ttu-id="13ec5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="13ec5-148">System.String</span></span>

### <span data-ttu-id="13ec5-149">System. URI</span><span class="sxs-lookup"><span data-stu-id="13ec5-149">System.Uri</span></span>

### <span data-ttu-id="13ec5-150">Microsoft. Azure. commands. kiszámítás. models. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="13ec5-150">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="13ec5-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13ec5-151">OUTPUTS</span></span>

### <span data-ttu-id="13ec5-152">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="13ec5-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="13ec5-153">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="13ec5-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="13ec5-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13ec5-154">NOTES</span></span>

## <span data-ttu-id="13ec5-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13ec5-155">RELATED LINKS</span></span>

[<span data-ttu-id="13ec5-156">Új – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="13ec5-156">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="13ec5-157">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="13ec5-157">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="13ec5-158">Újraindítás – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="13ec5-158">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="13ec5-159">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="13ec5-159">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="13ec5-160">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="13ec5-160">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="13ec5-161">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="13ec5-161">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


