---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: e29eb849dfd7ec3417daaea1b0cae447d20f1322
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499655"
---
# <span data-ttu-id="4dd2f-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4dd2f-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="4dd2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4dd2f-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd2f-103">Frissíti az Azure Virtual Machine állapotát.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dd2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4dd2f-104">SYNTAX</span></span>

### <span data-ttu-id="4dd2f-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4dd2f-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd2f-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dd2f-106">AssignIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd2f-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dd2f-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4dd2f-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4dd2f-108">IdParameterSetName</span></span>
```
Update-AzureRmVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4dd2f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="4dd2f-109">DESCRIPTION</span></span>
<span data-ttu-id="4dd2f-110">Az **Update-AzureRmVM** parancsmag az Azure virtuális gép állapotát egy virtuálisgép-objektum állapotát frissíti.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-110">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="4dd2f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4dd2f-111">EXAMPLES</span></span>

### <span data-ttu-id="4dd2f-112">Példa 1: virtuális gép frissítése</span><span class="sxs-lookup"><span data-stu-id="4dd2f-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="4dd2f-113">Ez a parancs frissíti a virtuális gépet, $VirtualMachine a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="4dd2f-114">A parancs a $VirtualMachine változóban tárolt virtuálisgép-objektum segítségével frissíti azt.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4dd2f-115">Virtuális gép objektum beszerzéséhez használja a **Get-AzureRmVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-115">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="4dd2f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4dd2f-116">PARAMETERS</span></span>

### <span data-ttu-id="4dd2f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4dd2f-117">-AsJob</span></span>
<span data-ttu-id="4dd2f-118">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4dd2f-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4dd2f-119">-AssignIdentity</span></span>
<span data-ttu-id="4dd2f-120">Adja meg a virtuális gép rendszerhez rendelt identitását.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-120">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="4dd2f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd2f-121">-DefaultProfile</span></span>
<span data-ttu-id="4dd2f-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dd2f-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="4dd2f-123">-Id</span></span>
<span data-ttu-id="4dd2f-124">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-124">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="4dd2f-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="4dd2f-125">-IdentityId</span></span>
<span data-ttu-id="4dd2f-126">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="4dd2f-127">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="4dd2f-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4dd2f-128">-IdentityType</span></span>
<span data-ttu-id="4dd2f-129">A virtuális géphez használt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="4dd2f-130">Jelenleg az egyetlen támogatott típus az "SystemAssigned", amely implicit módon létrehoz egy identitást.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="4dd2f-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="4dd2f-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="4dd2f-132">Megadja, hogy az operációs rendszer merevlemezén engedélyezni vagy tiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="4dd2f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd2f-133">-ResourceGroupName</span></span>
<span data-ttu-id="4dd2f-134">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4dd2f-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="4dd2f-135">-Tag</span></span>
<span data-ttu-id="4dd2f-136">Itt adhatja meg, hogy az erőforrások és az erőforráscsoport a name-Value pairek halmazával legyen címkézve.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="4dd2f-137">Ha címkéket ad az erőforrásokhoz, az erőforrásokat csoportosíthatja az erőforráscsoportok között, és saját nézeteket hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="4dd2f-138">Minden erőforrás vagy erőforráscsoport legfeljebb 15 címkét tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="4dd2f-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="4dd2f-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="4dd2f-140">Az a jelző, amely lehetővé teszi, hogy egy vagy több felügyelt adatlemez legyen a VM-ben UltraSSD_LRS tárterület-típussal.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="4dd2f-141">A felügyelt lemezek tároló fiók típusú UltraSSD_LRS csak akkor adhatók hozzá a virtuális géphez, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="4dd2f-142">-VM</span><span class="sxs-lookup"><span data-stu-id="4dd2f-142">-VM</span></span>
<span data-ttu-id="4dd2f-143">A helyi virtuális gép objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="4dd2f-144">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-144">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="4dd2f-145">Ez a virtuálisgép-objektum a virtuális gép frissített állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="4dd2f-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4dd2f-146">-Confirm</span></span>
<span data-ttu-id="4dd2f-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dd2f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd2f-148">-WhatIf</span></span>
<span data-ttu-id="4dd2f-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dd2f-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4dd2f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dd2f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd2f-151">CommonParameters</span></span>
<span data-ttu-id="4dd2f-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4dd2f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd2f-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dd2f-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd2f-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dd2f-154">INPUTS</span></span>

### <span data-ttu-id="4dd2f-155">System. String</span><span class="sxs-lookup"><span data-stu-id="4dd2f-155">System.String</span></span>

### <span data-ttu-id="4dd2f-156">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4dd2f-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4dd2f-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dd2f-157">OUTPUTS</span></span>

### <span data-ttu-id="4dd2f-158">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4dd2f-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4dd2f-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4dd2f-159">NOTES</span></span>

## <span data-ttu-id="4dd2f-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4dd2f-160">RELATED LINKS</span></span>

[<span data-ttu-id="4dd2f-161">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4dd2f-161">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="4dd2f-162">Új – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4dd2f-162">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="4dd2f-163">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4dd2f-163">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="4dd2f-164">Újraindítás – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4dd2f-164">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="4dd2f-165">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4dd2f-165">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="4dd2f-166">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4dd2f-166">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="4dd2f-167">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="4dd2f-167">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


