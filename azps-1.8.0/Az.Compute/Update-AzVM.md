---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e87536a524766ac86b80d790ee1372336fedba17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836597"
---
# <span data-ttu-id="ec265-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ec265-101">Update-AzVM</span></span>

## <span data-ttu-id="ec265-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec265-102">SYNOPSIS</span></span>
<span data-ttu-id="ec265-103">Frissíti az Azure Virtual Machine állapotát.</span><span class="sxs-lookup"><span data-stu-id="ec265-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="ec265-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec265-104">SYNTAX</span></span>

### <span data-ttu-id="ec265-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec265-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec265-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec265-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec265-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec265-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec265-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ec265-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec265-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec265-109">DESCRIPTION</span></span>
<span data-ttu-id="ec265-110">Az **Update-AzVM** parancsmag az Azure virtuális gép állapotát egy virtuálisgép-objektum állapotát frissíti.</span><span class="sxs-lookup"><span data-stu-id="ec265-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="ec265-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ec265-111">EXAMPLES</span></span>

### <span data-ttu-id="ec265-112">Példa 1: virtuális gép frissítése</span><span class="sxs-lookup"><span data-stu-id="ec265-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="ec265-113">Ez a parancs frissíti a virtuális gépet, $VirtualMachine a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="ec265-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="ec265-114">A parancs a $VirtualMachine változóban tárolt virtuálisgép-objektum segítségével frissíti azt.</span><span class="sxs-lookup"><span data-stu-id="ec265-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ec265-115">Virtuális gép objektum beszerzéséhez használja a **Get-AzVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ec265-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="ec265-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec265-116">PARAMETERS</span></span>

### <span data-ttu-id="ec265-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec265-117">-AsJob</span></span>
<span data-ttu-id="ec265-118">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="ec265-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ec265-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ec265-119">-AssignIdentity</span></span>
<span data-ttu-id="ec265-120">Adja meg a virtuális gép rendszerhez rendelt identitását.</span><span class="sxs-lookup"><span data-stu-id="ec265-120">Specify the system-assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec265-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec265-121">-DefaultProfile</span></span>
<span data-ttu-id="ec265-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec265-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec265-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ec265-123">-Id</span></span>
<span data-ttu-id="ec265-124">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec265-124">Specifies the resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec265-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="ec265-125">-IdentityId</span></span>
<span data-ttu-id="ec265-126">A virtuális géppel társított felhasználói azonosítók listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec265-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="ec265-127">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="ec265-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec265-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ec265-128">-IdentityType</span></span>
<span data-ttu-id="ec265-129">A virtuális géphez használt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="ec265-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="ec265-130">Az érvényes értékek a következők: SystemAssigned, UserAssigned, SystemAssignedUserAssigned és nincs.</span><span class="sxs-lookup"><span data-stu-id="ec265-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec265-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="ec265-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="ec265-132">Megadja, hogy az operációs rendszer merevlemezén engedélyezni vagy tiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="ec265-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec265-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec265-133">-ResourceGroupName</span></span>
<span data-ttu-id="ec265-134">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec265-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec265-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="ec265-135">-Tag</span></span>
<span data-ttu-id="ec265-136">Itt adhatja meg, hogy az erőforrások és az erőforráscsoport a name-Value pairek halmazával legyen címkézve.</span><span class="sxs-lookup"><span data-stu-id="ec265-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="ec265-137">Ha címkéket ad az erőforrásokhoz, az erőforrásokat csoportosíthatja az erőforráscsoportok között, és saját nézeteket hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="ec265-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="ec265-138">Minden erőforrás vagy erőforráscsoport legfeljebb 15 címkét tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="ec265-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec265-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="ec265-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="ec265-140">Az a jelző, amely lehetővé teszi, hogy egy vagy több felügyelt adatlemez legyen a VM-ben UltraSSD_LRS tárterület-típussal.</span><span class="sxs-lookup"><span data-stu-id="ec265-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="ec265-141">A felügyelt lemezek tároló fiók típusú UltraSSD_LRS csak akkor adhatók hozzá a virtuális géphez, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="ec265-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec265-142">-VM</span><span class="sxs-lookup"><span data-stu-id="ec265-142">-VM</span></span>
<span data-ttu-id="ec265-143">A helyi virtuális gép objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec265-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="ec265-144">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ec265-144">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="ec265-145">Ez a virtuálisgép-objektum a virtuális gép frissített állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ec265-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec265-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ec265-146">-Confirm</span></span>
<span data-ttu-id="ec265-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec265-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec265-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec265-148">-WhatIf</span></span>
<span data-ttu-id="ec265-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ec265-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec265-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec265-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec265-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec265-151">CommonParameters</span></span>
<span data-ttu-id="ec265-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec265-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec265-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec265-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec265-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec265-154">INPUTS</span></span>

### <span data-ttu-id="ec265-155">System. String</span><span class="sxs-lookup"><span data-stu-id="ec265-155">System.String</span></span>

### <span data-ttu-id="ec265-156">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ec265-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ec265-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec265-157">System.Boolean</span></span>

## <span data-ttu-id="ec265-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec265-158">OUTPUTS</span></span>

### <span data-ttu-id="ec265-159">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ec265-159">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ec265-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec265-160">NOTES</span></span>

## <span data-ttu-id="ec265-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec265-161">RELATED LINKS</span></span>

[<span data-ttu-id="ec265-162">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ec265-162">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ec265-163">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="ec265-163">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="ec265-164">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="ec265-164">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="ec265-165">Újraindítás – AzVM</span><span class="sxs-lookup"><span data-stu-id="ec265-165">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="ec265-166">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="ec265-166">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="ec265-167">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="ec265-167">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="ec265-168">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ec265-168">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


