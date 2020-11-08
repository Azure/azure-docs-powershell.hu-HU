---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: 9b35e76b6c64373a39bd3e14f8c1697c7c5f3baf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012894"
---
# <span data-ttu-id="1db95-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="1db95-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="1db95-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1db95-102">SYNOPSIS</span></span>
<span data-ttu-id="1db95-103">Egy virtuális gép DSC-bővítményének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1db95-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="1db95-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1db95-104">SYNTAX</span></span>

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1db95-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1db95-105">DESCRIPTION</span></span>
<span data-ttu-id="1db95-106">A **Get-AzVMDscExtensionStatus** parancsmag az erőforráscsoport egy virtuális gépén a kívánt állapotot (DSC) tartalmazó bővítmény állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1db95-106">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="1db95-107">A konfiguráció alkalmazásakor a parancsmag a Start-DscConfiguration parancsmaggal összhangban lévő kimenetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1db95-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="1db95-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1db95-108">EXAMPLES</span></span>

## <span data-ttu-id="1db95-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1db95-109">PARAMETERS</span></span>

### <span data-ttu-id="1db95-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db95-110">-DefaultProfile</span></span>
<span data-ttu-id="1db95-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1db95-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1db95-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1db95-112">-Name</span></span>
<span data-ttu-id="1db95-113">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1db95-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="1db95-114">A Set-AzVMDscExtension parancsmag ezt a nevet a Microsoft. PowerShell. DSC értékre állítja be, amely a **Get-AzVMDscExtensionStatus** által használt érték.</span><span class="sxs-lookup"><span data-stu-id="1db95-114">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="1db95-115">Csak akkor adja meg ezt a paramétert, ha módosította az alapértelmezett nevet a set parancsmagban, vagy másik erőforrás nevét használta egy erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="1db95-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="1db95-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1db95-116">-ResourceGroupName</span></span>
<span data-ttu-id="1db95-117">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1db95-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1db95-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="1db95-118">-VMName</span></span>
<span data-ttu-id="1db95-119">Annak a virtuális gépnek a neve, amelyhez ez a parancsmag a DSC kiterjesztési állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="1db95-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="1db95-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db95-120">CommonParameters</span></span>
<span data-ttu-id="1db95-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1db95-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db95-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1db95-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db95-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1db95-123">INPUTS</span></span>

### <span data-ttu-id="1db95-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1db95-124">System.String</span></span>

## <span data-ttu-id="1db95-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1db95-125">OUTPUTS</span></span>

### <span data-ttu-id="1db95-126">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="1db95-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="1db95-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1db95-127">NOTES</span></span>

## <span data-ttu-id="1db95-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1db95-128">RELATED LINKS</span></span>

[<span data-ttu-id="1db95-129">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="1db95-129">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


