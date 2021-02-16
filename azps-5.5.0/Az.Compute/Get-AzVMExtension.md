---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: ca9693f715d72366a6cc78030d0a8328bf0abc50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204903"
---
# <span data-ttu-id="c1622-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="c1622-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="c1622-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1622-102">SYNOPSIS</span></span>
<span data-ttu-id="c1622-103">Virtuális gépre telepített virtuálisgép-bővítmények tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c1622-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="c1622-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c1622-104">SYNTAX</span></span>

### <span data-ttu-id="c1622-105">GetExtensionParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1622-105">GetExtensionParameterSet (Default)</span></span>
```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1622-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1622-106">VMParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-VMObject <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1622-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1622-107">ResourceIdParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-ResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1622-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c1622-108">DESCRIPTION</span></span>
<span data-ttu-id="c1622-109">A **Get-AzVMExtension** parancsmag virtuális gépre telepített Virtuálisgép-bővítmények tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c1622-109">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="c1622-110">Adja meg annak a bővítménynek a nevét, amelynek tulajdonságait meg kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="c1622-110">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="c1622-111">Ha egy bővítménynek csak a példánynézetét meg kell adnia, adja meg az Állapot paramétert.</span><span class="sxs-lookup"><span data-stu-id="c1622-111">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="c1622-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c1622-112">EXAMPLES</span></span>

### <span data-ttu-id="c1622-113">1. példa: Bővítmény tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="c1622-113">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="c1622-114">Ez a parancs a CustomScriptExtension nevű bővítmény tulajdonságait kapja meg az ResourceGroup11 erőforráscsoport VirtualMachine22 nevű virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="c1622-114">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="c1622-115">2. példa: Bővítmény példánynézetének lekérte</span><span class="sxs-lookup"><span data-stu-id="c1622-115">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                : {Microsoft.Azure.Management.Compute.Models.InstanceViewStatus}
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="c1622-116">Ez a parancs a CustomScriptExtension nevű bővítmény példánynézetét kapja meg az ResourceGroup11 erőforráscsoport VirtualMachine22 nevű virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="c1622-116">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="c1622-117">3. példa: Az összes bővítmény telepítése VM-en</span><span class="sxs-lookup"><span data-stu-id="c1622-117">Example 3: Get all extensions installed on a VM</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

### <span data-ttu-id="c1622-118">4. példa: Bővítmény tulajdonságainak lekérte a VM paramétert használva</span><span class="sxs-lookup"><span data-stu-id="c1622-118">Example 4: Get properties of an extension using the VM parameter</span></span>
```
PS C:\> $vm = Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine22"
PS C:\> Get-AzVMExtension -VM $vm

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="c1622-119">Ez a parancs az ResourceGroup11 erőforráscsoport VirtualMachine22 nevű virtuális gépére telepíti a bővítmények listáját.</span><span class="sxs-lookup"><span data-stu-id="c1622-119">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="c1622-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1622-120">PARAMETERS</span></span>

### <span data-ttu-id="c1622-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1622-121">-DefaultProfile</span></span>
<span data-ttu-id="c1622-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1622-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1622-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c1622-123">-Name</span></span>
<span data-ttu-id="c1622-124">Egy bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1622-124">Specifies the name of an extension.</span></span>
<span data-ttu-id="c1622-125">Ez a parancsmag a paraméter által megadott kiterjesztés tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c1622-125">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1622-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1622-126">-ResourceGroupName</span></span>
<span data-ttu-id="c1622-127">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1622-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1622-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1622-128">-ResourceId</span></span>
<span data-ttu-id="c1622-129">Erőforrás-azonosító, amely megadja azt a virtuális gépi objektumot, amely a bővítményt be van va.</span><span class="sxs-lookup"><span data-stu-id="c1622-129">Resource Id specifying the virtual machine object the extension is on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1622-130">-Állapot</span><span class="sxs-lookup"><span data-stu-id="c1622-130">-Status</span></span>
<span data-ttu-id="c1622-131">Azt jelzi, hogy ez a parancsmag csak egy bővítmény példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c1622-131">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1622-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="c1622-132">-VMName</span></span>
<span data-ttu-id="c1622-133">Egy virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1622-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c1622-134">Ez a parancsmag a paraméter által megadott virtuális gép egyik bővítményének tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c1622-134">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1622-135">-VMObject</span><span class="sxs-lookup"><span data-stu-id="c1622-135">-VMObject</span></span>
<span data-ttu-id="c1622-136">Azt a virtuális gépobjektumot adja meg, amelybe a bővítmény be van stb.</span><span class="sxs-lookup"><span data-stu-id="c1622-136">Specifies the virtual machine object the extension is on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1622-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1622-137">CommonParameters</span></span>
<span data-ttu-id="c1622-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1622-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1622-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1622-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1622-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1622-140">INPUTS</span></span>

### <span data-ttu-id="c1622-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c1622-141">System.String</span></span>

### <span data-ttu-id="c1622-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c1622-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c1622-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1622-143">OUTPUTS</span></span>

### <span data-ttu-id="c1622-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="c1622-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="c1622-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c1622-145">NOTES</span></span>

## <span data-ttu-id="c1622-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1622-146">RELATED LINKS</span></span>

[<span data-ttu-id="c1622-147">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="c1622-147">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="c1622-148">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="c1622-148">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


