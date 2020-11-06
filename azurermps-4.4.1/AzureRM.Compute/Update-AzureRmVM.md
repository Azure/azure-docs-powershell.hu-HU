---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: ad337c07f22b2805002347758f91bf0ea781adad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499176"
---
# <span data-ttu-id="f4824-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f4824-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="f4824-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4824-102">SYNOPSIS</span></span>
<span data-ttu-id="f4824-103">Frissíti az Azure Virtual Machine állapotát.</span><span class="sxs-lookup"><span data-stu-id="f4824-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4824-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4824-104">SYNTAX</span></span>

### <span data-ttu-id="f4824-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4824-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4824-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f4824-106">IdParameterSetName</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4824-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4824-107">DESCRIPTION</span></span>
<span data-ttu-id="f4824-108">Az **Update-AzureRmVM** parancsmag az Azure virtuális gép állapotát egy virtuálisgép-objektum állapotát frissíti.</span><span class="sxs-lookup"><span data-stu-id="f4824-108">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="f4824-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f4824-109">EXAMPLES</span></span>

### <span data-ttu-id="f4824-110">Példa 1: virtuális gép frissítése</span><span class="sxs-lookup"><span data-stu-id="f4824-110">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="f4824-111">Ez a parancs frissíti a virtuális gépet, $VirtualMachine a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="f4824-111">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="f4824-112">A parancs a $VirtualMachine változóban tárolt virtuálisgép-objektum segítségével frissíti azt.</span><span class="sxs-lookup"><span data-stu-id="f4824-112">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f4824-113">Virtuális gép objektum beszerzéséhez használja a **Get-AzureRmVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f4824-113">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="f4824-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4824-114">PARAMETERS</span></span>

### <span data-ttu-id="f4824-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f4824-115">-AssignIdentity</span></span>
<span data-ttu-id="f4824-116">Adja meg a virtuális gép rendszerhez rendelt identitását.</span><span class="sxs-lookup"><span data-stu-id="f4824-116">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="f4824-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4824-117">-DefaultProfile</span></span>
<span data-ttu-id="f4824-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4824-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4824-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f4824-119">-Id</span></span>
<span data-ttu-id="f4824-120">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4824-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="f4824-121">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f4824-121">-IdentityType</span></span>
<span data-ttu-id="f4824-122">A virtuális géphez használt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="f4824-122">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="f4824-123">Jelenleg az egyetlen támogatott típus az "SystemAssigned", amely implicit módon létrehoz egy identitást.</span><span class="sxs-lookup"><span data-stu-id="f4824-123">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4824-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4824-124">-ResourceGroupName</span></span>
<span data-ttu-id="f4824-125">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4824-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4824-126">-Címkék</span><span class="sxs-lookup"><span data-stu-id="f4824-126">-Tags</span></span>
<span data-ttu-id="f4824-127">Itt adhatja meg, hogy az erőforrások és az erőforráscsoport a name-Value pairek halmazával legyen címkézve.</span><span class="sxs-lookup"><span data-stu-id="f4824-127">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="f4824-128">Ha címkéket ad az erőforrásokhoz, az erőforrásokat csoportosíthatja az erőforráscsoportok között, és saját nézeteket hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="f4824-128">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="f4824-129">Minden erőforrás vagy erőforráscsoport legfeljebb 15 címkét tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="f4824-129">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="f4824-130">-VM</span><span class="sxs-lookup"><span data-stu-id="f4824-130">-VM</span></span>
<span data-ttu-id="f4824-131">A helyi virtuális gép objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4824-131">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="f4824-132">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f4824-132">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="f4824-133">Ez a virtuálisgép-objektum a virtuális gép frissített állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f4824-133">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="f4824-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4824-134">-Confirm</span></span>
<span data-ttu-id="f4824-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4824-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4824-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4824-136">-WhatIf</span></span>
<span data-ttu-id="f4824-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4824-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f4824-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4824-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4824-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4824-139">CommonParameters</span></span>
<span data-ttu-id="f4824-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4824-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4824-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4824-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4824-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4824-142">INPUTS</span></span>

## <span data-ttu-id="f4824-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4824-143">OUTPUTS</span></span>

## <span data-ttu-id="f4824-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4824-144">NOTES</span></span>

## <span data-ttu-id="f4824-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4824-145">RELATED LINKS</span></span>

[<span data-ttu-id="f4824-146">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f4824-146">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="f4824-147">Új – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f4824-147">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="f4824-148">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f4824-148">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="f4824-149">Újraindítás – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f4824-149">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="f4824-150">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f4824-150">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="f4824-151">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f4824-151">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="f4824-152">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="f4824-152">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


