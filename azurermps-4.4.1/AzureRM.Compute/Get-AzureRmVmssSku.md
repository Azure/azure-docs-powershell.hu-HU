---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: ef814121aab7a78150689b876e36d88993be4747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505188"
---
# <span data-ttu-id="b56ff-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="b56ff-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="b56ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b56ff-102">SYNOPSIS</span></span>
<span data-ttu-id="b56ff-103">A VMSS elérhető SKU-ket kapja.</span><span class="sxs-lookup"><span data-stu-id="b56ff-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b56ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b56ff-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b56ff-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b56ff-105">DESCRIPTION</span></span>
<span data-ttu-id="b56ff-106">A **Get-AzureRmVmssSku** parancsmag a virtuálisgép-készlet (VMSS) számára elérhető SKU-ket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b56ff-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b56ff-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b56ff-107">EXAMPLES</span></span>

### <span data-ttu-id="b56ff-108">Példa 1: az összes elérhető SKU beszerzése a VMSS</span><span class="sxs-lookup"><span data-stu-id="b56ff-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="b56ff-109">Ez a parancs minden elérhető SKU-t beolvas a ContosoGroup nevű erőforráscsoport ContosoVMSS nevű VMSS.</span><span class="sxs-lookup"><span data-stu-id="b56ff-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="b56ff-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b56ff-110">PARAMETERS</span></span>

### <span data-ttu-id="b56ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b56ff-111">-DefaultProfile</span></span>
<span data-ttu-id="b56ff-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b56ff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b56ff-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b56ff-113">-ResourceGroupName</span></span>
<span data-ttu-id="b56ff-114">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b56ff-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="b56ff-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b56ff-115">-VMScaleSetName</span></span>
<span data-ttu-id="b56ff-116">Faj: a VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="b56ff-116">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b56ff-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56ff-117">CommonParameters</span></span>
<span data-ttu-id="b56ff-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b56ff-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56ff-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b56ff-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56ff-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b56ff-120">INPUTS</span></span>

## <span data-ttu-id="b56ff-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b56ff-121">OUTPUTS</span></span>

### <span data-ttu-id="b56ff-122">Ez a parancsmag nem hoz létre semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="b56ff-122">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="b56ff-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b56ff-123">NOTES</span></span>

## <span data-ttu-id="b56ff-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b56ff-124">RELATED LINKS</span></span>

[<span data-ttu-id="b56ff-125">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b56ff-125">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


