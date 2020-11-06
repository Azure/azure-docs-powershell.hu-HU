---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 0a14bf4f2c8a4b686f222079cadaec1744e41d08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500896"
---
# <span data-ttu-id="62472-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="62472-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="62472-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62472-102">SYNOPSIS</span></span>
<span data-ttu-id="62472-103">Egy virtuális gép DSC-bővítményének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="62472-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62472-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62472-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62472-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="62472-105">DESCRIPTION</span></span>
<span data-ttu-id="62472-106">A **Get-AzureRmVMDscExtensionStatus** parancsmag az erőforráscsoport egy virtuális gépén a kívánt állapotot (DSC) tartalmazó bővítmény állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="62472-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="62472-107">A konfiguráció alkalmazásakor a parancsmag a Start-DscConfiguration parancsmaggal összhangban lévő kimenetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="62472-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="62472-108">Példák</span><span class="sxs-lookup"><span data-stu-id="62472-108">EXAMPLES</span></span>

## <span data-ttu-id="62472-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62472-109">PARAMETERS</span></span>

### <span data-ttu-id="62472-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62472-110">-DefaultProfile</span></span>
<span data-ttu-id="62472-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62472-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62472-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62472-112">-Name</span></span>
<span data-ttu-id="62472-113">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62472-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="62472-114">A Set-AzureRmVMDscExtension parancsmag ezt a nevet a Microsoft. PowerShell. DSC értékre állítja be, amely a **Get-AzureRmVMDscExtensionStatus** által használt érték.</span><span class="sxs-lookup"><span data-stu-id="62472-114">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="62472-115">Csak akkor adja meg ezt a paramétert, ha módosította az alapértelmezett nevet a set parancsmagban, vagy másik erőforrás nevét használta egy erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="62472-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="62472-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62472-116">-ResourceGroupName</span></span>
<span data-ttu-id="62472-117">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62472-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="62472-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="62472-118">-VMName</span></span>
<span data-ttu-id="62472-119">Annak a virtuális gépnek a neve, amelyhez ez a parancsmag a DSC kiterjesztési állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="62472-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="62472-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62472-120">CommonParameters</span></span>
<span data-ttu-id="62472-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62472-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62472-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62472-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62472-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62472-123">INPUTS</span></span>

## <span data-ttu-id="62472-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62472-124">OUTPUTS</span></span>

## <span data-ttu-id="62472-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62472-125">NOTES</span></span>

## <span data-ttu-id="62472-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62472-126">RELATED LINKS</span></span>

[<span data-ttu-id="62472-127">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="62472-127">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


