---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: b89bf343c1737080867bbe5e8cb5397fd52f6a4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919017"
---
# <span data-ttu-id="ea7ba-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="ea7ba-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="ea7ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea7ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7ba-103">A VMSS-hez elérhető SKUs-okat kapja.</span><span class="sxs-lookup"><span data-stu-id="ea7ba-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="ea7ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ea7ba-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea7ba-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ea7ba-105">DESCRIPTION</span></span>
<span data-ttu-id="ea7ba-106">A **Get-AzVmssSku** parancsmag megkapja a virtuálisgép-mérethalmazhoz (VMSS) elérhető termékváltozatokat.</span><span class="sxs-lookup"><span data-stu-id="ea7ba-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ea7ba-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ea7ba-107">EXAMPLES</span></span>

### <span data-ttu-id="ea7ba-108">1. példa: Az összes elérhető SKUs lekérte a VMSS-ről</span><span class="sxs-lookup"><span data-stu-id="ea7ba-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ea7ba-109">Ez a parancs a ContosoVMSS nevű VMSS-hez tartozó összes elérhető SKUs-t beveszi a ContosoGroup nevű erőforráscsoportba.</span><span class="sxs-lookup"><span data-stu-id="ea7ba-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="ea7ba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea7ba-110">PARAMETERS</span></span>

### <span data-ttu-id="ea7ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7ba-111">-DefaultProfile</span></span>
<span data-ttu-id="ea7ba-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea7ba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea7ba-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea7ba-113">-ResourceGroupName</span></span>
<span data-ttu-id="ea7ba-114">A VMSS erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea7ba-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="ea7ba-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ea7ba-115">-VMScaleSetName</span></span>
<span data-ttu-id="ea7ba-116">A VMSS nevének fakása.</span><span class="sxs-lookup"><span data-stu-id="ea7ba-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="ea7ba-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7ba-117">CommonParameters</span></span>
<span data-ttu-id="ea7ba-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea7ba-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7ba-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea7ba-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7ba-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea7ba-120">INPUTS</span></span>

### <span data-ttu-id="ea7ba-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ea7ba-121">System.String</span></span>

## <span data-ttu-id="ea7ba-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea7ba-122">OUTPUTS</span></span>

### <span data-ttu-id="ea7ba-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="ea7ba-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="ea7ba-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ea7ba-124">NOTES</span></span>

## <span data-ttu-id="ea7ba-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea7ba-125">RELATED LINKS</span></span>

[<span data-ttu-id="ea7ba-126">Get-AzVms</span><span class="sxs-lookup"><span data-stu-id="ea7ba-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


