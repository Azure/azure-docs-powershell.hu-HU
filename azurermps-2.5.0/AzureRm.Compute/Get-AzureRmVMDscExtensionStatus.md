---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextensionstatus
schema: 2.0.0
ms.openlocfilehash: b6ec9918657c191e31e10c04b799603654d39d56
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848334"
---
# <span data-ttu-id="72dc2-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="72dc2-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="72dc2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="72dc2-103">Egy virtuális gép DSC-bővítményének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72dc2-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72dc2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72dc2-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72dc2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72dc2-105">DESCRIPTION</span></span>
<span data-ttu-id="72dc2-106">A **Get-AzureRmVMDscExtensionStatus** parancsmag az erőforráscsoport egy virtuális gépén a kívánt állapotot (DSC) tartalmazó bővítmény állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72dc2-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="72dc2-107">A konfiguráció alkalmazásakor a parancsmag a Start-DscConfiguration parancsmaggal összhangban lévő kimenetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="72dc2-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="72dc2-108">Példák</span><span class="sxs-lookup"><span data-stu-id="72dc2-108">EXAMPLES</span></span>

### <span data-ttu-id="72dc2-109">1:</span><span class="sxs-lookup"><span data-stu-id="72dc2-109">1:</span></span>
```

```

## <span data-ttu-id="72dc2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72dc2-110">PARAMETERS</span></span>

### <span data-ttu-id="72dc2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72dc2-111">-DefaultProfile</span></span>
<span data-ttu-id="72dc2-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72dc2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72dc2-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72dc2-113">-Name</span></span>
<span data-ttu-id="72dc2-114">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72dc2-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="72dc2-115">A Set-AzureRmVMDscExtension parancsmag ezt a nevet a Microsoft. PowerShell. DSC értékre állítja be, amely a **Get-AzureRmVMDscExtensionStatus** által használt érték.</span><span class="sxs-lookup"><span data-stu-id="72dc2-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="72dc2-116">Csak akkor adja meg ezt a paramétert, ha módosította az alapértelmezett nevet a set parancsmagban, vagy másik erőforrás nevét használta egy erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="72dc2-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="72dc2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72dc2-117">-ResourceGroupName</span></span>
<span data-ttu-id="72dc2-118">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72dc2-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="72dc2-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="72dc2-119">-VMName</span></span>
<span data-ttu-id="72dc2-120">Annak a virtuális gépnek a neve, amelyhez ez a parancsmag a DSC kiterjesztési állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="72dc2-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="72dc2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72dc2-121">CommonParameters</span></span>
<span data-ttu-id="72dc2-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72dc2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72dc2-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72dc2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72dc2-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72dc2-124">INPUTS</span></span>

### <span data-ttu-id="72dc2-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="72dc2-125">None</span></span>
<span data-ttu-id="72dc2-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="72dc2-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72dc2-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72dc2-127">OUTPUTS</span></span>

### <span data-ttu-id="72dc2-128">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="72dc2-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="72dc2-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72dc2-129">NOTES</span></span>

## <span data-ttu-id="72dc2-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72dc2-130">RELATED LINKS</span></span>

[<span data-ttu-id="72dc2-131">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="72dc2-131">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


