---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: ba4ac8d48c72ffac164e447777670c48f529f68f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328996"
---
# <span data-ttu-id="385fa-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="385fa-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="385fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="385fa-102">SYNOPSIS</span></span>
<span data-ttu-id="385fa-103">A DSC-bővítmény beállításait egy adott virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="385fa-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="385fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="385fa-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="385fa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="385fa-105">DESCRIPTION</span></span>
<span data-ttu-id="385fa-106">A **Get-AzVMDscExtension** parancsmag egy adott virtuális gépen megkapja a kívánt államkonfigurációs (DSC) bővítmény beállításait.</span><span class="sxs-lookup"><span data-stu-id="385fa-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="385fa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="385fa-107">EXAMPLES</span></span>

### <span data-ttu-id="385fa-108">1. példa: DSC-bővítmény beállításainak lekérte</span><span class="sxs-lookup"><span data-stu-id="385fa-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="385fa-109">Ez a parancs a VM07 nevű virtuális gépen a DSC nevű bővítmény beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="385fa-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="385fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="385fa-110">PARAMETERS</span></span>

### <span data-ttu-id="385fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385fa-111">-DefaultProfile</span></span>
<span data-ttu-id="385fa-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="385fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="385fa-113">-Name</span><span class="sxs-lookup"><span data-stu-id="385fa-113">-Name</span></span>
<span data-ttu-id="385fa-114">Megadja a bővítményt képviselő Azure Resource Manager-erőforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="385fa-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="385fa-115">A Set-AzVMDscExtension parancsmag ezt a nevet a Microsoft.Powershell.DSC értékre állítja, amely megegyezik a **Get-AzVMDscExtension** által használt értékkel.</span><span class="sxs-lookup"><span data-stu-id="385fa-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="385fa-116">Ezt a paramétert csak akkor adja meg, ha módosította az alapértelmezett nevet a **Set-AzVMDscExtension** parancsmagban, vagy másik erőforrásnevet használt egy Erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="385fa-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385fa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="385fa-117">-ResourceGroupName</span></span>
<span data-ttu-id="385fa-118">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="385fa-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="385fa-119">-Állapot</span><span class="sxs-lookup"><span data-stu-id="385fa-119">-Status</span></span>
<span data-ttu-id="385fa-120">Azt jelzi, hogy ez a parancsmag a DSC kiterjesztés példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="385fa-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="385fa-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="385fa-121">-VMName</span></span>
<span data-ttu-id="385fa-122">Annak a virtuális gépnek a nevét adja meg, amelynek a parancsmagja DSC kiterjesztést kap.</span><span class="sxs-lookup"><span data-stu-id="385fa-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385fa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385fa-123">CommonParameters</span></span>
<span data-ttu-id="385fa-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385fa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385fa-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="385fa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385fa-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="385fa-126">INPUTS</span></span>

### <span data-ttu-id="385fa-127">System.String</span><span class="sxs-lookup"><span data-stu-id="385fa-127">System.String</span></span>

### <span data-ttu-id="385fa-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="385fa-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="385fa-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="385fa-129">OUTPUTS</span></span>

### <span data-ttu-id="385fa-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="385fa-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="385fa-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="385fa-131">NOTES</span></span>

## <span data-ttu-id="385fa-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="385fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="385fa-133">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="385fa-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="385fa-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="385fa-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


