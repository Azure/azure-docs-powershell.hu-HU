---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: 2c36408b520268acaaa6ae2fa4c4c6030fbd2111
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347718"
---
# <span data-ttu-id="0cf54-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0cf54-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="0cf54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cf54-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf54-103">Virtuális gépre telepített virtuálisgép-bővítmények tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0cf54-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="0cf54-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0cf54-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cf54-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0cf54-105">DESCRIPTION</span></span>
<span data-ttu-id="0cf54-106">A **Get-AzVMExtension** parancsmag virtuális gépre telepített Virtuálisgép-bővítmények tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0cf54-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="0cf54-107">Adja meg annak a bővítménynek a nevét, amelynek tulajdonságait meg kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="0cf54-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="0cf54-108">Ha egy bővítménynek csak a példánynézetét meg kell adnia, adja meg az Állapot paramétert.</span><span class="sxs-lookup"><span data-stu-id="0cf54-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="0cf54-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0cf54-109">EXAMPLES</span></span>

### <span data-ttu-id="0cf54-110">1. példa: Bővítmény tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="0cf54-110">Example 1: Get properties of an extension</span></span>
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

<span data-ttu-id="0cf54-111">Ez a parancs a CustomScriptExtension nevű bővítmény tulajdonságait kapja meg az ResourceGroup11 erőforráscsoport VirtualMachine22 nevű virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="0cf54-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="0cf54-112">2. példa: Bővítmény példánynézetének lekérte</span><span class="sxs-lookup"><span data-stu-id="0cf54-112">Example 2: Get instance view of an extension</span></span>
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

<span data-ttu-id="0cf54-113">Ez a parancs a CustomScriptExtension nevű bővítmény példánynézetét kapja meg az ResourceGroup11 erőforráscsoport VirtualMachine22 nevű virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="0cf54-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="0cf54-114">3. példa: Az összes bővítmény telepítése VM-en</span><span class="sxs-lookup"><span data-stu-id="0cf54-114">Example 3: Get all extensions installed on a VM</span></span>
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

<span data-ttu-id="0cf54-115">Ez a parancs az ResourceGroup11 erőforráscsoport VirtualMachine22 nevű virtuális gépére telepíti a bővítmények listáját.</span><span class="sxs-lookup"><span data-stu-id="0cf54-115">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="0cf54-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cf54-116">PARAMETERS</span></span>

### <span data-ttu-id="0cf54-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf54-117">-DefaultProfile</span></span>
<span data-ttu-id="0cf54-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cf54-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cf54-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0cf54-119">-Name</span></span>
<span data-ttu-id="0cf54-120">Egy bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0cf54-120">Specifies the name of an extension.</span></span>
<span data-ttu-id="0cf54-121">Ez a parancsmag a paraméter által megadott kiterjesztés tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0cf54-121">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="0cf54-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cf54-122">-ResourceGroupName</span></span>
<span data-ttu-id="0cf54-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0cf54-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0cf54-124">-Állapot</span><span class="sxs-lookup"><span data-stu-id="0cf54-124">-Status</span></span>
<span data-ttu-id="0cf54-125">Azt jelzi, hogy ez a parancsmag csak egy bővítmény példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0cf54-125">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="0cf54-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="0cf54-126">-VMName</span></span>
<span data-ttu-id="0cf54-127">Egy virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0cf54-127">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0cf54-128">Ez a parancsmag a paraméter által megadott virtuális gép egyik bővítményének tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0cf54-128">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="0cf54-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf54-129">CommonParameters</span></span>
<span data-ttu-id="0cf54-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf54-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf54-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cf54-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf54-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0cf54-132">INPUTS</span></span>

### <span data-ttu-id="0cf54-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0cf54-133">System.String</span></span>

### <span data-ttu-id="0cf54-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0cf54-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0cf54-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cf54-135">OUTPUTS</span></span>

### <span data-ttu-id="0cf54-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="0cf54-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="0cf54-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0cf54-137">NOTES</span></span>

## <span data-ttu-id="0cf54-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cf54-138">RELATED LINKS</span></span>

[<span data-ttu-id="0cf54-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0cf54-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="0cf54-140">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0cf54-140">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


