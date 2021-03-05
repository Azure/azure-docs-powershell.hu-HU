---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: 307dccf0d5bb137ba83a6acf3a9b5db0b4606f7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013846"
---
# <span data-ttu-id="c8350-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c8350-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="c8350-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8350-102">SYNOPSIS</span></span>
<span data-ttu-id="c8350-103">A DSC-bővítmény beállításait egy adott virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c8350-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="c8350-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c8350-104">SYNTAX</span></span>

### <span data-ttu-id="c8350-105">GetDscExtension (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8350-105">GetDscExtension (Default)</span></span>
```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8350-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8350-106">VMParameterSet</span></span>
```
Get-AzVMDscExtension [-Status] [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8350-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c8350-107">DESCRIPTION</span></span>
<span data-ttu-id="c8350-108">A **Get-AzVMDscExtension** parancsmag egy adott virtuális gépen megkapja a kívánt államkonfigurációs (DSC) bővítmény beállításait.</span><span class="sxs-lookup"><span data-stu-id="c8350-108">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="c8350-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c8350-109">EXAMPLES</span></span>

### <span data-ttu-id="c8350-110">1. példa: DSC-bővítmény beállításainak lekérte</span><span class="sxs-lookup"><span data-stu-id="c8350-110">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="c8350-111">Ez a parancs a VM07 nevű virtuális gépen a DSC nevű bővítmény beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c8350-111">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="c8350-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8350-112">PARAMETERS</span></span>

### <span data-ttu-id="c8350-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8350-113">-DefaultProfile</span></span>
<span data-ttu-id="c8350-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8350-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8350-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c8350-115">-Name</span></span>
<span data-ttu-id="c8350-116">Megadja a bővítményt képviselő Azure Resource Manager-erőforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="c8350-116">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="c8350-117">A Set-AzVMDscExtension parancsmag ezt a nevet a Microsoft.Powershell.DSC értékre állítja, amely megegyezik a **Get-AzVMDscExtension** által használt értékkel.</span><span class="sxs-lookup"><span data-stu-id="c8350-117">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="c8350-118">Ezt a paramétert csak akkor adja meg, ha módosította az alapértelmezett nevet a **Set-AzVMDscExtension** parancsmagban, vagy másik erőforrásnevet használt egy Erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="c8350-118">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8350-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8350-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8350-120">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8350-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8350-121">-Állapot</span><span class="sxs-lookup"><span data-stu-id="c8350-121">-Status</span></span>
<span data-ttu-id="c8350-122">Azt jelzi, hogy ez a parancsmag a DSC kiterjesztés példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c8350-122">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8350-123">-VM</span><span class="sxs-lookup"><span data-stu-id="c8350-123">-VM</span></span>
<span data-ttu-id="c8350-124">Azt a virtuális gépobjektumot adja meg, amelybe a bővítmény be van stb.</span><span class="sxs-lookup"><span data-stu-id="c8350-124">Specifies the virtual machine object the extension is on.</span></span>

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

### <span data-ttu-id="c8350-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="c8350-125">-VMName</span></span>
<span data-ttu-id="c8350-126">Annak a virtuális gépnek a nevét adja meg, amelynek a parancsmagja DSC kiterjesztést kap.</span><span class="sxs-lookup"><span data-stu-id="c8350-126">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8350-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8350-127">CommonParameters</span></span>
<span data-ttu-id="c8350-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8350-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8350-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8350-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8350-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8350-130">INPUTS</span></span>

### <span data-ttu-id="c8350-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c8350-131">System.String</span></span>

### <span data-ttu-id="c8350-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c8350-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c8350-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8350-133">OUTPUTS</span></span>

### <span data-ttu-id="c8350-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="c8350-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="c8350-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c8350-135">NOTES</span></span>

## <span data-ttu-id="c8350-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8350-136">RELATED LINKS</span></span>

[<span data-ttu-id="c8350-137">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c8350-137">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="c8350-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c8350-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


