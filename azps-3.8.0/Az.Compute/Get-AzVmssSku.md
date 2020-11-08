---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002938"
---
# <span data-ttu-id="de2ee-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="de2ee-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="de2ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de2ee-102">SYNOPSIS</span></span>
<span data-ttu-id="de2ee-103">A VMSS elérhető SKU-ket kapja.</span><span class="sxs-lookup"><span data-stu-id="de2ee-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="de2ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de2ee-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de2ee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de2ee-105">DESCRIPTION</span></span>
<span data-ttu-id="de2ee-106">A **Get-AzVmssSku** parancsmag a virtuálisgép-készlet (VMSS) számára elérhető SKU-ket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="de2ee-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="de2ee-107">Példák</span><span class="sxs-lookup"><span data-stu-id="de2ee-107">EXAMPLES</span></span>

### <span data-ttu-id="de2ee-108">Példa 1: az összes elérhető SKU beszerzése a VMSS</span><span class="sxs-lookup"><span data-stu-id="de2ee-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="de2ee-109">Ez a parancs minden elérhető SKU-t beolvas a ContosoGroup nevű erőforráscsoport ContosoVMSS nevű VMSS.</span><span class="sxs-lookup"><span data-stu-id="de2ee-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="de2ee-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de2ee-110">PARAMETERS</span></span>

### <span data-ttu-id="de2ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de2ee-111">-DefaultProfile</span></span>
<span data-ttu-id="de2ee-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de2ee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de2ee-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de2ee-113">-ResourceGroupName</span></span>
<span data-ttu-id="de2ee-114">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de2ee-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="de2ee-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="de2ee-115">-VMScaleSetName</span></span>
<span data-ttu-id="de2ee-116">Faj: a VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="de2ee-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="de2ee-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de2ee-117">CommonParameters</span></span>
<span data-ttu-id="de2ee-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de2ee-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de2ee-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="de2ee-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de2ee-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de2ee-120">INPUTS</span></span>

### <span data-ttu-id="de2ee-121">System. String</span><span class="sxs-lookup"><span data-stu-id="de2ee-121">System.String</span></span>

## <span data-ttu-id="de2ee-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de2ee-122">OUTPUTS</span></span>

### <span data-ttu-id="de2ee-123">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="de2ee-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="de2ee-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de2ee-124">NOTES</span></span>

## <span data-ttu-id="de2ee-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de2ee-125">RELATED LINKS</span></span>

[<span data-ttu-id="de2ee-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="de2ee-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


