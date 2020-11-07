---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: f861465fcc9f27f71142ffd4e49935039f3da9c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671344"
---
# <span data-ttu-id="c5914-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="c5914-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="c5914-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5914-102">SYNOPSIS</span></span>
<span data-ttu-id="c5914-103">A virtuálisgép-bővítmények tulajdonságait a virtuális gépen telepítette.</span><span class="sxs-lookup"><span data-stu-id="c5914-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="c5914-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5914-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5914-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5914-105">DESCRIPTION</span></span>
<span data-ttu-id="c5914-106">A **Get-AzVMExtension** parancsmag a virtuális gépre telepített virtuálisgép-bővítmények tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c5914-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="c5914-107">Adja meg annak a bővítménynek a nevét, amelyhez tulajdonságokat szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="c5914-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="c5914-108">Ha csak a bővítmény példány nézetét szeretné látni, adja meg az állapot paramétert.</span><span class="sxs-lookup"><span data-stu-id="c5914-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="c5914-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c5914-109">EXAMPLES</span></span>

### <span data-ttu-id="c5914-110">Példa 1: bővítmény tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="c5914-110">Example 1: Get properties of an extension</span></span>
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

<span data-ttu-id="c5914-111">Ez a parancs a CustomScriptExtension nevű bővítmény tulajdonságait az erőforráscsoport ResourceGroup11 VirtualMachine22 nevű virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c5914-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="c5914-112">2. példa: egy bővítmény példány nézetének beolvasása</span><span class="sxs-lookup"><span data-stu-id="c5914-112">Example 2: Get instance view of an extension</span></span>
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

<span data-ttu-id="c5914-113">Ez a parancs a CustomScriptExtension nevű VirtualMachine22 nevű virtuális gép példány nézetét kapja meg az erőforráscsoport ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c5914-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="c5914-114">3. példa: a VM-be telepített összes bővítmény beolvasása</span><span class="sxs-lookup"><span data-stu-id="c5914-114">Example 3: Get all extensions installed on a VM</span></span>
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

<span data-ttu-id="c5914-115">Ez a parancs a VirtualMachine22 nevű virtuális gépre telepített bővítmények listáját kapja meg az erőforráscsoport ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c5914-115">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="c5914-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5914-116">PARAMETERS</span></span>

### <span data-ttu-id="c5914-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5914-117">-DefaultProfile</span></span>
<span data-ttu-id="c5914-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5914-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5914-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5914-119">-Name</span></span>
<span data-ttu-id="c5914-120">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5914-120">Specifies the name of an extension.</span></span>
<span data-ttu-id="c5914-121">Ez a parancsmag a paraméter által megadott kiterjesztés tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c5914-121">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5914-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5914-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5914-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5914-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5914-124">-Állapot</span><span class="sxs-lookup"><span data-stu-id="c5914-124">-Status</span></span>
<span data-ttu-id="c5914-125">Jelzi, hogy ez a parancsmag csak a bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c5914-125">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="c5914-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="c5914-126">-VMName</span></span>
<span data-ttu-id="c5914-127">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5914-127">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c5914-128">Ez a parancsmag a virtuális gép egy bővítményének tulajdonságait adja meg, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5914-128">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5914-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5914-129">CommonParameters</span></span>
<span data-ttu-id="c5914-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5914-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5914-131">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c5914-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5914-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5914-132">INPUTS</span></span>

### <span data-ttu-id="c5914-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c5914-133">System.String</span></span>

### <span data-ttu-id="c5914-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c5914-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c5914-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5914-135">OUTPUTS</span></span>

### <span data-ttu-id="c5914-136">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="c5914-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="c5914-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5914-137">NOTES</span></span>

## <span data-ttu-id="c5914-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5914-138">RELATED LINKS</span></span>

[<span data-ttu-id="c5914-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="c5914-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="c5914-140">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="c5914-140">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


