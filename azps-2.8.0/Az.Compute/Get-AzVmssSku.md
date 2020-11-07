---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: a7696ee9738a885d3edea1eb8a3d2f9f7cea8510
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667409"
---
# <span data-ttu-id="69c9f-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="69c9f-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="69c9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="69c9f-103">A VMSS elérhető SKU-ket kapja.</span><span class="sxs-lookup"><span data-stu-id="69c9f-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="69c9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69c9f-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69c9f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69c9f-105">DESCRIPTION</span></span>
<span data-ttu-id="69c9f-106">A **Get-AzVmssSku** parancsmag a virtuálisgép-készlet (VMSS) számára elérhető SKU-ket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="69c9f-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="69c9f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69c9f-107">EXAMPLES</span></span>

### <span data-ttu-id="69c9f-108">Példa 1: az összes elérhető SKU beszerzése a VMSS</span><span class="sxs-lookup"><span data-stu-id="69c9f-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="69c9f-109">Ez a parancs minden elérhető SKU-t beolvas a ContosoGroup nevű erőforráscsoport ContosoVMSS nevű VMSS.</span><span class="sxs-lookup"><span data-stu-id="69c9f-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="69c9f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69c9f-110">PARAMETERS</span></span>

### <span data-ttu-id="69c9f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c9f-111">-DefaultProfile</span></span>
<span data-ttu-id="69c9f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69c9f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69c9f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c9f-113">-ResourceGroupName</span></span>
<span data-ttu-id="69c9f-114">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69c9f-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="69c9f-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="69c9f-115">-VMScaleSetName</span></span>
<span data-ttu-id="69c9f-116">Faj: a VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="69c9f-116">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c9f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c9f-117">CommonParameters</span></span>
<span data-ttu-id="69c9f-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69c9f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c9f-119">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="69c9f-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c9f-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69c9f-120">INPUTS</span></span>

### <span data-ttu-id="69c9f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="69c9f-121">System.String</span></span>

## <span data-ttu-id="69c9f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69c9f-122">OUTPUTS</span></span>

### <span data-ttu-id="69c9f-123">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="69c9f-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="69c9f-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69c9f-124">NOTES</span></span>

## <span data-ttu-id="69c9f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69c9f-125">RELATED LINKS</span></span>

[<span data-ttu-id="69c9f-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="69c9f-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


