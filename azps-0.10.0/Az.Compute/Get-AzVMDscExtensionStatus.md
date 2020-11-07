---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: 3ae9827c6db5136b9327936a63ac0441dcf94ff1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844594"
---
# <span data-ttu-id="1854f-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="1854f-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="1854f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1854f-102">SYNOPSIS</span></span>
<span data-ttu-id="1854f-103">Egy virtuális gép DSC-bővítményének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1854f-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="1854f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1854f-104">SYNTAX</span></span>

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1854f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1854f-105">DESCRIPTION</span></span>
<span data-ttu-id="1854f-106">A **Get-AzVMDscExtensionStatus** parancsmag az erőforráscsoport egy virtuális gépén a kívánt állapotot (DSC) tartalmazó bővítmény állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1854f-106">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="1854f-107">A konfiguráció alkalmazásakor a parancsmag a Start-DscConfiguration parancsmaggal összhangban lévő kimenetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1854f-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="1854f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1854f-108">EXAMPLES</span></span>

### <span data-ttu-id="1854f-109">1:</span><span class="sxs-lookup"><span data-stu-id="1854f-109">1:</span></span>
```

```

## <span data-ttu-id="1854f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1854f-110">PARAMETERS</span></span>

### <span data-ttu-id="1854f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1854f-111">-DefaultProfile</span></span>
<span data-ttu-id="1854f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1854f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1854f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1854f-113">-Name</span></span>
<span data-ttu-id="1854f-114">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1854f-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="1854f-115">A Set-AzVMDscExtension parancsmag ezt a nevet a Microsoft. PowerShell. DSC értékre állítja be, amely a **Get-AzVMDscExtensionStatus** által használt érték.</span><span class="sxs-lookup"><span data-stu-id="1854f-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="1854f-116">Csak akkor adja meg ezt a paramétert, ha módosította az alapértelmezett nevet a set parancsmagban, vagy másik erőforrás nevét használta egy erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="1854f-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1854f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1854f-117">-ResourceGroupName</span></span>
<span data-ttu-id="1854f-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1854f-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1854f-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="1854f-119">-VMName</span></span>
<span data-ttu-id="1854f-120">Annak a virtuális gépnek a neve, amelyhez ez a parancsmag a DSC kiterjesztési állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="1854f-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1854f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1854f-121">CommonParameters</span></span>
<span data-ttu-id="1854f-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1854f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1854f-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1854f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1854f-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1854f-124">INPUTS</span></span>

### <span data-ttu-id="1854f-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="1854f-125">None</span></span>
<span data-ttu-id="1854f-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1854f-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1854f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1854f-127">OUTPUTS</span></span>

### <span data-ttu-id="1854f-128">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="1854f-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="1854f-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1854f-129">NOTES</span></span>

## <span data-ttu-id="1854f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1854f-130">RELATED LINKS</span></span>

[<span data-ttu-id="1854f-131">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="1854f-131">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


