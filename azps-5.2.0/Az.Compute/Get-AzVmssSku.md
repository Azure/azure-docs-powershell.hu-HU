---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368925"
---
# <span data-ttu-id="c9d95-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="c9d95-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="c9d95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9d95-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d95-103">A VMSS-hez elérhető SKUs-okat kapja.</span><span class="sxs-lookup"><span data-stu-id="c9d95-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="c9d95-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c9d95-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9d95-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c9d95-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d95-106">A **Get-AzVmssSku** parancsmag megkapja a virtuálisgép-mérethalmazhoz (VMSS) elérhető termékváltozatokat.</span><span class="sxs-lookup"><span data-stu-id="c9d95-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="c9d95-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c9d95-107">EXAMPLES</span></span>

### <span data-ttu-id="c9d95-108">1. példa: Az összes elérhető SKUs lekérte a VMSS-ről</span><span class="sxs-lookup"><span data-stu-id="c9d95-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="c9d95-109">Ez a parancs a ContosoVMSS nevű VMSS-hez tartozó összes elérhető SKUs-t beveszi a ContosoGroup nevű erőforráscsoportba.</span><span class="sxs-lookup"><span data-stu-id="c9d95-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="c9d95-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9d95-110">PARAMETERS</span></span>

### <span data-ttu-id="c9d95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d95-111">-DefaultProfile</span></span>
<span data-ttu-id="c9d95-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9d95-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9d95-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d95-113">-ResourceGroupName</span></span>
<span data-ttu-id="c9d95-114">A VMSS erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9d95-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="c9d95-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c9d95-115">-VMScaleSetName</span></span>
<span data-ttu-id="c9d95-116">A VMSS nevének fakása.</span><span class="sxs-lookup"><span data-stu-id="c9d95-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="c9d95-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d95-117">CommonParameters</span></span>
<span data-ttu-id="c9d95-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d95-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d95-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9d95-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d95-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9d95-120">INPUTS</span></span>

### <span data-ttu-id="c9d95-121">System.String</span><span class="sxs-lookup"><span data-stu-id="c9d95-121">System.String</span></span>

## <span data-ttu-id="c9d95-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9d95-122">OUTPUTS</span></span>

### <span data-ttu-id="c9d95-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="c9d95-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="c9d95-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c9d95-124">NOTES</span></span>

## <span data-ttu-id="c9d95-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9d95-125">RELATED LINKS</span></span>

[<span data-ttu-id="c9d95-126">Get-AzVms</span><span class="sxs-lookup"><span data-stu-id="c9d95-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


