---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 6be4e505dfdacdc95e6ab3c9f7229fa4d1e470f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012564"
---
# <span data-ttu-id="dba9d-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="dba9d-101">Update-AzVM</span></span>

## <span data-ttu-id="dba9d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dba9d-102">SYNOPSIS</span></span>
<span data-ttu-id="dba9d-103">Frissíti az Azure Virtual Machine állapotát.</span><span class="sxs-lookup"><span data-stu-id="dba9d-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="dba9d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dba9d-104">SYNTAX</span></span>

### <span data-ttu-id="dba9d-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dba9d-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba9d-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="dba9d-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba9d-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="dba9d-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba9d-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="dba9d-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dba9d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="dba9d-109">DESCRIPTION</span></span>
<span data-ttu-id="dba9d-110">Az **Update-AzVM** parancsmag az Azure virtuális gép állapotát egy virtuálisgép-objektum állapotát frissíti.</span><span class="sxs-lookup"><span data-stu-id="dba9d-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="dba9d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="dba9d-111">EXAMPLES</span></span>

### <span data-ttu-id="dba9d-112">Példa 1: virtuális gép frissítése</span><span class="sxs-lookup"><span data-stu-id="dba9d-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="dba9d-113">Ez a parancs frissíti a virtuális gépet, $VirtualMachine a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="dba9d-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="dba9d-114">A parancs a $VirtualMachine változóban tárolt virtuálisgép-objektum segítségével frissíti azt.</span><span class="sxs-lookup"><span data-stu-id="dba9d-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="dba9d-115">Virtuális gép objektum beszerzéséhez használja a **Get-AzVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dba9d-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="dba9d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dba9d-116">PARAMETERS</span></span>

### <span data-ttu-id="dba9d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dba9d-117">-AsJob</span></span>
<span data-ttu-id="dba9d-118">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="dba9d-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="dba9d-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="dba9d-119">-AssignIdentity</span></span>
<span data-ttu-id="dba9d-120">Adja meg a virtuális gép rendszerhez rendelt identitását.</span><span class="sxs-lookup"><span data-stu-id="dba9d-120">Specify the system-assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="dba9d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba9d-121">-DefaultProfile</span></span>
<span data-ttu-id="dba9d-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dba9d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dba9d-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="dba9d-123">-Id</span></span>
<span data-ttu-id="dba9d-124">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dba9d-124">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="dba9d-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="dba9d-125">-IdentityId</span></span>
<span data-ttu-id="dba9d-126">A virtuális géppel társított felhasználói azonosítók listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dba9d-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="dba9d-127">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="dba9d-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="dba9d-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="dba9d-128">-IdentityType</span></span>
<span data-ttu-id="dba9d-129">A virtuális géphez használt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="dba9d-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="dba9d-130">Az érvényes értékek a következők: SystemAssigned, UserAssigned, SystemAssignedUserAssigned és nincs.</span><span class="sxs-lookup"><span data-stu-id="dba9d-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="dba9d-131">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="dba9d-131">-MaxPrice</span></span>
<span data-ttu-id="dba9d-132">Itt adhatja meg, hogy az alacsony prioritású VM/VMSS milyen maximális árat fizessen.</span><span class="sxs-lookup"><span data-stu-id="dba9d-132">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="dba9d-133">Ez az ár amerikai dollárban van.</span><span class="sxs-lookup"><span data-stu-id="dba9d-133">This price is in US Dollars.</span></span> <span data-ttu-id="dba9d-134">Ezt az árat a program összehasonlítja a VM-méret jelenlegi alacsony prioritási árával.</span><span class="sxs-lookup"><span data-stu-id="dba9d-134">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="dba9d-135">Az árakat az alacsony prioritású VM/VMSS létrehozásának/frissítésének időpontjában is összehasonlították, és a művelet csak akkor fog sikerülni, ha a maxPrice nagyobb, mint a jelenlegi alacsony prioritású ár.</span><span class="sxs-lookup"><span data-stu-id="dba9d-135">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="dba9d-136">A maxPrice a VM/VMSS létrehozása után is az alacsony prioritású VM/VMSS eltávolítására használható, ha a jelenlegi alacsony prioritású ár túllépi a maxPrice.</span><span class="sxs-lookup"><span data-stu-id="dba9d-136">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="dba9d-137">Lehetséges értékek: bármely nullánál nagyobb decimális érték.</span><span class="sxs-lookup"><span data-stu-id="dba9d-137">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="dba9d-138">Példa: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="dba9d-138">Example: 0.01538.</span></span>  <span data-ttu-id="dba9d-139">-1 – azt jelzi, hogy az alacsony prioritású VM/VMSS nem szabad az árak miatt kizárni.</span><span class="sxs-lookup"><span data-stu-id="dba9d-139">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="dba9d-140">Az alapértelmezett Max ár is-1, ha az nem az Ön által megadott.</span><span class="sxs-lookup"><span data-stu-id="dba9d-140">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dba9d-141">-Várva</span><span class="sxs-lookup"><span data-stu-id="dba9d-141">-NoWait</span></span>
<span data-ttu-id="dba9d-142">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="dba9d-142">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="dba9d-143">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="dba9d-143">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="dba9d-144">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="dba9d-144">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="dba9d-145">Megadja, hogy az operációs rendszer merevlemezén engedélyezni vagy tiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="dba9d-145">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="dba9d-146">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="dba9d-146">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="dba9d-147">Az ezzel a virtuális géppel használható közelségi hely csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dba9d-147">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dba9d-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba9d-148">-ResourceGroupName</span></span>
<span data-ttu-id="dba9d-149">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dba9d-149">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="dba9d-150">-Címke</span><span class="sxs-lookup"><span data-stu-id="dba9d-150">-Tag</span></span>
<span data-ttu-id="dba9d-151">Itt adhatja meg, hogy az erőforrások és az erőforráscsoport a name-Value pairek halmazával legyen címkézve.</span><span class="sxs-lookup"><span data-stu-id="dba9d-151">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="dba9d-152">Ha címkéket ad az erőforrásokhoz, az erőforrásokat csoportosíthatja az erőforráscsoportok között, és saját nézeteket hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="dba9d-152">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="dba9d-153">Minden erőforrás vagy erőforráscsoport legfeljebb 15 címkét tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="dba9d-153">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="dba9d-154">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="dba9d-154">-UltraSSDEnabled</span></span>
<span data-ttu-id="dba9d-155">Az a jelző, amely lehetővé teszi, hogy egy vagy több felügyelt adatlemez legyen a VM-ben UltraSSD_LRS tárterület-típussal.</span><span class="sxs-lookup"><span data-stu-id="dba9d-155">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="dba9d-156">A felügyelt lemezek tároló fiók típusú UltraSSD_LRS csak akkor adhatók hozzá a virtuális géphez, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="dba9d-156">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="dba9d-157">-VM</span><span class="sxs-lookup"><span data-stu-id="dba9d-157">-VM</span></span>
<span data-ttu-id="dba9d-158">A helyi virtuális gép objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dba9d-158">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="dba9d-159">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dba9d-159">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="dba9d-160">Ez a virtuálisgép-objektum a virtuális gép frissített állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="dba9d-160">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="dba9d-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dba9d-161">-Confirm</span></span>
<span data-ttu-id="dba9d-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dba9d-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dba9d-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dba9d-163">-WhatIf</span></span>
<span data-ttu-id="dba9d-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dba9d-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dba9d-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dba9d-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dba9d-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba9d-166">CommonParameters</span></span>
<span data-ttu-id="dba9d-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dba9d-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba9d-168">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dba9d-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba9d-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dba9d-169">INPUTS</span></span>

### <span data-ttu-id="dba9d-170">System. String</span><span class="sxs-lookup"><span data-stu-id="dba9d-170">System.String</span></span>

### <span data-ttu-id="dba9d-171">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dba9d-171">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="dba9d-172">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dba9d-172">System.Boolean</span></span>

## <span data-ttu-id="dba9d-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dba9d-173">OUTPUTS</span></span>

### <span data-ttu-id="dba9d-174">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="dba9d-174">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="dba9d-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dba9d-175">NOTES</span></span>

## <span data-ttu-id="dba9d-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dba9d-176">RELATED LINKS</span></span>

[<span data-ttu-id="dba9d-177">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="dba9d-177">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="dba9d-178">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="dba9d-178">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="dba9d-179">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="dba9d-179">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="dba9d-180">Újraindítás – AzVM</span><span class="sxs-lookup"><span data-stu-id="dba9d-180">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="dba9d-181">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="dba9d-181">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="dba9d-182">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="dba9d-182">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="dba9d-183">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="dba9d-183">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


