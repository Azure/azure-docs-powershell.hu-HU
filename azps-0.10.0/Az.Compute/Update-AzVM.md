---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 8dd18c97a1636e4b6422d58fa7aca28d8798001b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842430"
---
# <span data-ttu-id="bec8c-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bec8c-101">Update-AzVM</span></span>

## <span data-ttu-id="bec8c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bec8c-102">SYNOPSIS</span></span>
<span data-ttu-id="bec8c-103">Frissíti az Azure Virtual Machine állapotát.</span><span class="sxs-lookup"><span data-stu-id="bec8c-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="bec8c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bec8c-104">SYNTAX</span></span>

### <span data-ttu-id="bec8c-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bec8c-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bec8c-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="bec8c-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bec8c-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="bec8c-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec8c-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bec8c-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bec8c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="bec8c-109">DESCRIPTION</span></span>
<span data-ttu-id="bec8c-110">Az **Update-AzVM** parancsmag az Azure virtuális gép állapotát egy virtuálisgép-objektum állapotát frissíti.</span><span class="sxs-lookup"><span data-stu-id="bec8c-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="bec8c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="bec8c-111">EXAMPLES</span></span>

### <span data-ttu-id="bec8c-112">Példa 1: virtuális gép frissítése</span><span class="sxs-lookup"><span data-stu-id="bec8c-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="bec8c-113">Ez a parancs frissíti a virtuális gépet, $VirtualMachine a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="bec8c-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="bec8c-114">A parancs a $VirtualMachine változóban tárolt virtuálisgép-objektum segítségével frissíti azt.</span><span class="sxs-lookup"><span data-stu-id="bec8c-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="bec8c-115">Virtuális gép objektum beszerzéséhez használja a **Get-AzVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bec8c-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="bec8c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bec8c-116">PARAMETERS</span></span>

### <span data-ttu-id="bec8c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bec8c-117">-AsJob</span></span>
<span data-ttu-id="bec8c-118">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="bec8c-118">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec8c-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="bec8c-119">-AssignIdentity</span></span>
<span data-ttu-id="bec8c-120">Adja meg a virtuális gép rendszerhez rendelt identitását.</span><span class="sxs-lookup"><span data-stu-id="bec8c-120">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec8c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec8c-121">-DefaultProfile</span></span>
<span data-ttu-id="bec8c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bec8c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bec8c-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="bec8c-123">-Id</span></span>
<span data-ttu-id="bec8c-124">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bec8c-124">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec8c-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="bec8c-125">-IdentityId</span></span>
<span data-ttu-id="bec8c-126">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bec8c-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="bec8c-127">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="bec8c-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec8c-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="bec8c-128">-IdentityType</span></span>
<span data-ttu-id="bec8c-129">A virtuális géphez használt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="bec8c-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="bec8c-130">Jelenleg az egyetlen támogatott típus az "SystemAssigned", amely implicit módon létrehoz egy identitást.</span><span class="sxs-lookup"><span data-stu-id="bec8c-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec8c-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="bec8c-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="bec8c-132">Megadja, hogy az operációs rendszer merevlemezén engedélyezni vagy tiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="bec8c-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec8c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec8c-133">-ResourceGroupName</span></span>
<span data-ttu-id="bec8c-134">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bec8c-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec8c-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="bec8c-135">-Tag</span></span>
<span data-ttu-id="bec8c-136">Itt adhatja meg, hogy az erőforrások és az erőforráscsoport a name-Value pairek halmazával legyen címkézve.</span><span class="sxs-lookup"><span data-stu-id="bec8c-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="bec8c-137">Ha címkéket ad az erőforrásokhoz, az erőforrásokat csoportosíthatja az erőforráscsoportok között, és saját nézeteket hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="bec8c-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="bec8c-138">Minden erőforrás vagy erőforráscsoport legfeljebb 15 címkét tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="bec8c-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec8c-139">-VM</span><span class="sxs-lookup"><span data-stu-id="bec8c-139">-VM</span></span>
<span data-ttu-id="bec8c-140">A helyi virtuális gép objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bec8c-140">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="bec8c-141">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bec8c-141">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="bec8c-142">Ez a virtuálisgép-objektum a virtuális gép frissített állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bec8c-142">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bec8c-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bec8c-143">-Confirm</span></span>
<span data-ttu-id="bec8c-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bec8c-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec8c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec8c-145">-WhatIf</span></span>
<span data-ttu-id="bec8c-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bec8c-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="bec8c-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bec8c-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec8c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec8c-148">CommonParameters</span></span>
<span data-ttu-id="bec8c-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bec8c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec8c-150">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec8c-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec8c-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bec8c-151">INPUTS</span></span>

### <span data-ttu-id="bec8c-152">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bec8c-152">PSVirtualMachine</span></span>
<span data-ttu-id="bec8c-153">A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="bec8c-153">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="bec8c-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bec8c-154">OUTPUTS</span></span>

### <span data-ttu-id="bec8c-155">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bec8c-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bec8c-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bec8c-156">NOTES</span></span>

## <span data-ttu-id="bec8c-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bec8c-157">RELATED LINKS</span></span>

[<span data-ttu-id="bec8c-158">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="bec8c-158">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="bec8c-159">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="bec8c-159">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="bec8c-160">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="bec8c-160">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="bec8c-161">Újraindítás – AzVM</span><span class="sxs-lookup"><span data-stu-id="bec8c-161">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="bec8c-162">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="bec8c-162">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="bec8c-163">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="bec8c-163">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="bec8c-164">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="bec8c-164">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


