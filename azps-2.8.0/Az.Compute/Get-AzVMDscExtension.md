---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: 0ae022c9a8755c0ffa8bdfeafa12ab18922214a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667440"
---
# <span data-ttu-id="507ba-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="507ba-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="507ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="507ba-102">SYNOPSIS</span></span>
<span data-ttu-id="507ba-103">Egy adott virtuális gépen a DSC bővítmény beállításait kapja.</span><span class="sxs-lookup"><span data-stu-id="507ba-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="507ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="507ba-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="507ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="507ba-105">DESCRIPTION</span></span>
<span data-ttu-id="507ba-106">A **Get-AzVMDscExtension** parancsmag az adott virtuális gépen a kívánt állapot-konfiguráció (DSC) kiterjesztésének beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="507ba-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="507ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="507ba-107">EXAMPLES</span></span>

### <span data-ttu-id="507ba-108">Példa 1: a DSC kiterjesztés beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="507ba-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="507ba-109">Ez a parancs a DSC nevű bővítmény beállítását a VM07 nevű virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="507ba-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="507ba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="507ba-110">PARAMETERS</span></span>

### <span data-ttu-id="507ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="507ba-111">-DefaultProfile</span></span>
<span data-ttu-id="507ba-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="507ba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="507ba-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="507ba-113">-Name</span></span>
<span data-ttu-id="507ba-114">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="507ba-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="507ba-115">A Set-AzVMDscExtension parancsmag ezt a nevet a Microsoft. PowerShell. DSC értékre állítja be, amely a **Get-AzVMDscExtension** által használt érték.</span><span class="sxs-lookup"><span data-stu-id="507ba-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="507ba-116">Csak akkor adja meg ezt a paramétert, ha módosította az alapértelmezett nevet a **set-AzVMDscExtension** parancsmagban, vagy másik erőforrás nevét használta egy erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="507ba-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="507ba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="507ba-117">-ResourceGroupName</span></span>
<span data-ttu-id="507ba-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="507ba-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="507ba-119">-Állapot</span><span class="sxs-lookup"><span data-stu-id="507ba-119">-Status</span></span>
<span data-ttu-id="507ba-120">Jelzi, hogy ez a parancsmag a DSC bővítmény példány nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="507ba-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="507ba-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="507ba-121">-VMName</span></span>
<span data-ttu-id="507ba-122">Annak a virtuális gépnek a neve, amelyhez a parancsmag a DSC kiterjesztést kapja.</span><span class="sxs-lookup"><span data-stu-id="507ba-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="507ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="507ba-123">CommonParameters</span></span>
<span data-ttu-id="507ba-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="507ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="507ba-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="507ba-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="507ba-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="507ba-126">INPUTS</span></span>

### <span data-ttu-id="507ba-127">System. String</span><span class="sxs-lookup"><span data-stu-id="507ba-127">System.String</span></span>

### <span data-ttu-id="507ba-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="507ba-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="507ba-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="507ba-129">OUTPUTS</span></span>

### <span data-ttu-id="507ba-130">Microsoft. Azure. commands. számítási. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="507ba-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="507ba-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="507ba-131">NOTES</span></span>

## <span data-ttu-id="507ba-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="507ba-132">RELATED LINKS</span></span>

[<span data-ttu-id="507ba-133">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="507ba-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="507ba-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="507ba-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


