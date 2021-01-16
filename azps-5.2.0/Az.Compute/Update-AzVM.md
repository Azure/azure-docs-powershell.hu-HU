---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e9ec68d7c3991d7a3eded2566d8e299ddcc36c85
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366980"
---
# <span data-ttu-id="e62c7-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e62c7-101">Update-AzVM</span></span>

## <span data-ttu-id="e62c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e62c7-102">SYNOPSIS</span></span>
<span data-ttu-id="e62c7-103">Frissíti egy Azure virtuális gép állapotát.</span><span class="sxs-lookup"><span data-stu-id="e62c7-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="e62c7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e62c7-104">SYNTAX</span></span>

### <span data-ttu-id="e62c7-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e62c7-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e62c7-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="e62c7-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e62c7-107">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e62c7-107">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e62c7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e62c7-108">DESCRIPTION</span></span>
<span data-ttu-id="e62c7-109">Az **Update-AzVM** parancsmag frissíti egy Azure virtuális gép állapotát egy virtuális gépi objektum állapotára.</span><span class="sxs-lookup"><span data-stu-id="e62c7-109">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="e62c7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e62c7-110">EXAMPLES</span></span>

### <span data-ttu-id="e62c7-111">1. példa: Virtuális gép frissítése</span><span class="sxs-lookup"><span data-stu-id="e62c7-111">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="e62c7-112">Ez a parancs frissíti a virtuális gépet, $VirtualMachine ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="e62c7-112">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="e62c7-113">A parancs frissíti azt a változóban tárolt virtuális $VirtualMachine használatával.</span><span class="sxs-lookup"><span data-stu-id="e62c7-113">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e62c7-114">Virtuális gépi objektum beszerzéséhez használja a **Get-AzVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e62c7-114">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="e62c7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e62c7-115">PARAMETERS</span></span>

### <span data-ttu-id="e62c7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e62c7-116">-AsJob</span></span>
<span data-ttu-id="e62c7-117">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="e62c7-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e62c7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62c7-118">-DefaultProfile</span></span>
<span data-ttu-id="e62c7-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e62c7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e62c7-120">-HostId</span><span class="sxs-lookup"><span data-stu-id="e62c7-120">-HostId</span></span>
<span data-ttu-id="e62c7-121">A host azonosítója</span><span class="sxs-lookup"><span data-stu-id="e62c7-121">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e62c7-122">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="e62c7-122">-EncryptionAtHost</span></span>
<span data-ttu-id="e62c7-123">A EncryptionAtHost tulajdonságot a felhasználó használhatja a kérésben a gazdatitkosítás engedélyezéséhez vagy letiltásához a virtuális gép vagy virtuális gép méretarányának beállítására.</span><span class="sxs-lookup"><span data-stu-id="e62c7-123">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="e62c7-124">Ez lehetővé teszi a titkosítást az összes lemezen, beleértve magában az erőforrás-/ideiglenes lemezen is.</span><span class="sxs-lookup"><span data-stu-id="e62c7-124">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62c7-125">-Id</span><span class="sxs-lookup"><span data-stu-id="e62c7-125">-Id</span></span>
<span data-ttu-id="e62c7-126">A virtuális gép erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e62c7-126">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="e62c7-127">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="e62c7-127">-IdentityId</span></span>
<span data-ttu-id="e62c7-128">A virtuális géphez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e62c7-128">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="e62c7-129">A felhasználói identitáshivatkozások ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="e62c7-129">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="e62c7-130">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e62c7-130">-IdentityType</span></span>
<span data-ttu-id="e62c7-131">A virtuális géphez használt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="e62c7-131">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="e62c7-132">Érvényes értékek: SystemAssigned, UserAssigned, SystemAssignedUserAssigned és None.</span><span class="sxs-lookup"><span data-stu-id="e62c7-132">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="e62c7-133">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="e62c7-133">-MaxPrice</span></span>
<span data-ttu-id="e62c7-134">Megadja az alacsony prioritású VM/VMSS-ek maximális árát.</span><span class="sxs-lookup"><span data-stu-id="e62c7-134">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="e62c7-135">Ez az ár amerikai dollárban van meg.</span><span class="sxs-lookup"><span data-stu-id="e62c7-135">This price is in US Dollars.</span></span> <span data-ttu-id="e62c7-136">Ezt az árat összehasonlítjuk a VM-méret jelenlegi alacsony prioritású árával.</span><span class="sxs-lookup"><span data-stu-id="e62c7-136">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="e62c7-137">Ezenkívül az alacsony prioritású VM/VMSS létrehozása/frissítése során összehasonlítja az árakat, és a művelet csak akkor lesz sikeres, ha a maxPrice nagyobb, mint a jelenlegi alacsony prioritású ár.</span><span class="sxs-lookup"><span data-stu-id="e62c7-137">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="e62c7-138">A maxPrice akkor is használatos az alacsony prioritású VM/VMSS kivül, ha a jelenlegi alacsony prioritású ár meghaladja a VM/VMSS létrehozását követően a maxPrice értéken.</span><span class="sxs-lookup"><span data-stu-id="e62c7-138">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="e62c7-139">A lehetséges értékek a nullánál nagyobb decimális értékek.</span><span class="sxs-lookup"><span data-stu-id="e62c7-139">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="e62c7-140">Példa: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="e62c7-140">Example: 0.01538.</span></span>  <span data-ttu-id="e62c7-141">-1 azt jelzi, hogy az alacsony prioritású VM/VMSS nem lesz kiváltva ár miatt.</span><span class="sxs-lookup"><span data-stu-id="e62c7-141">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="e62c7-142">Az alapértelmezett maximális ár -1, ha nem Ön biztosítja.</span><span class="sxs-lookup"><span data-stu-id="e62c7-142">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="e62c7-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e62c7-143">-NoWait</span></span>
<span data-ttu-id="e62c7-144">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="e62c7-144">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e62c7-145">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="e62c7-145">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e62c7-146">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e62c7-146">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="e62c7-147">Azt adja meg, hogy a WriteAccelerator engedélyezve vagy letiltva legyen-e az operációs rendszer lemezén.</span><span class="sxs-lookup"><span data-stu-id="e62c7-147">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="e62c7-148">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="e62c7-148">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="e62c7-149">Az ezzel a virtuális géppel használható Közelség elhelyezési csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e62c7-149">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="e62c7-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e62c7-150">-ResourceGroupName</span></span>
<span data-ttu-id="e62c7-151">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e62c7-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e62c7-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="e62c7-152">-Tag</span></span>
<span data-ttu-id="e62c7-153">Megadja, hogy mely erőforrások és erőforráscsoportok címkézhatók névérték-párokkal.</span><span class="sxs-lookup"><span data-stu-id="e62c7-153">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="e62c7-154">Ha címkéket ad az erőforrásokhoz, több erőforráscsoportban csoportosíthatók az erőforrások, és saját nézeteket hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="e62c7-154">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="e62c7-155">Minden erőforrás vagy erőforráscsoport legfeljebb 15 címkével lehet.</span><span class="sxs-lookup"><span data-stu-id="e62c7-155">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="e62c7-156">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="e62c7-156">-UltraSSDEnabled</span></span>
<span data-ttu-id="e62c7-157">A jelölő, amely lehetővé teszi vagy letiltja azt a lehetőséget, hogy egy vagy több felügyelt adatlemezzel UltraSSD_LRS tárfióktípussal a VM-en.</span><span class="sxs-lookup"><span data-stu-id="e62c7-157">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="e62c7-158">A tárfiók-típussal rendelkező felügyelt UltraSSD_LRS csak akkor lehet virtuális gépre hozzáadni, ha ez a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="e62c7-158">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="e62c7-159">-VM</span><span class="sxs-lookup"><span data-stu-id="e62c7-159">-VM</span></span>
<span data-ttu-id="e62c7-160">Egy helyi virtuális gépobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e62c7-160">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="e62c7-161">Virtuális gépi objektum beszerzéséhez használja a Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e62c7-161">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="e62c7-162">Ez a virtuális gépi objektum a virtuális gép frissített állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e62c7-162">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="e62c7-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e62c7-163">-Confirm</span></span>
<span data-ttu-id="e62c7-164">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e62c7-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e62c7-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e62c7-165">-WhatIf</span></span>
<span data-ttu-id="e62c7-166">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e62c7-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e62c7-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e62c7-167">The cmdlet is not run.</span></span>

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


### <span data-ttu-id="e62c7-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62c7-168">CommonParameters</span></span>
<span data-ttu-id="e62c7-169">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e62c7-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62c7-170">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e62c7-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62c7-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e62c7-171">INPUTS</span></span>

### <span data-ttu-id="e62c7-172">System.String</span><span class="sxs-lookup"><span data-stu-id="e62c7-172">System.String</span></span>

### <span data-ttu-id="e62c7-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e62c7-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e62c7-174">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e62c7-174">System.Boolean</span></span>

## <span data-ttu-id="e62c7-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e62c7-175">OUTPUTS</span></span>

### <span data-ttu-id="e62c7-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e62c7-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e62c7-177">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e62c7-177">NOTES</span></span>

## <span data-ttu-id="e62c7-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e62c7-178">RELATED LINKS</span></span>

[<span data-ttu-id="e62c7-179">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e62c7-179">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e62c7-180">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e62c7-180">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="e62c7-181">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="e62c7-181">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="e62c7-182">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="e62c7-182">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="e62c7-183">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="e62c7-183">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="e62c7-184">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="e62c7-184">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="e62c7-185">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e62c7-185">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


