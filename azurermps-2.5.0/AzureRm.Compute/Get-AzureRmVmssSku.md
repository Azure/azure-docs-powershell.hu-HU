---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsssku
schema: 2.0.0
ms.openlocfilehash: 307b9852f506368e1e13c02fac4532dab4d2ddd2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849773"
---
# <span data-ttu-id="d2d64-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="d2d64-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="d2d64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2d64-102">SYNOPSIS</span></span>
<span data-ttu-id="d2d64-103">A VMSS elérhető SKU-ket kapja.</span><span class="sxs-lookup"><span data-stu-id="d2d64-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2d64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2d64-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2d64-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2d64-105">DESCRIPTION</span></span>
<span data-ttu-id="d2d64-106">A **Get-AzureRmVmssSku** parancsmag a virtuálisgép-készlet (VMSS) számára elérhető SKU-ket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d2d64-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d2d64-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d2d64-107">EXAMPLES</span></span>

### <span data-ttu-id="d2d64-108">Példa 1: az összes elérhető SKU beszerzése a VMSS</span><span class="sxs-lookup"><span data-stu-id="d2d64-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="d2d64-109">Ez a parancs minden elérhető SKU-t beolvas a ContosoGroup nevű erőforráscsoport ContosoVMSS nevű VMSS.</span><span class="sxs-lookup"><span data-stu-id="d2d64-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="d2d64-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2d64-110">PARAMETERS</span></span>

### <span data-ttu-id="d2d64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2d64-111">-DefaultProfile</span></span>
<span data-ttu-id="d2d64-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2d64-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2d64-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2d64-113">-ResourceGroupName</span></span>
<span data-ttu-id="d2d64-114">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2d64-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="d2d64-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d2d64-115">-VMScaleSetName</span></span>
<span data-ttu-id="d2d64-116">Faj: a VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="d2d64-116">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2d64-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d64-117">CommonParameters</span></span>
<span data-ttu-id="d2d64-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2d64-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d64-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2d64-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d64-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2d64-120">INPUTS</span></span>

### <span data-ttu-id="d2d64-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="d2d64-121">None</span></span>
<span data-ttu-id="d2d64-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d2d64-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2d64-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2d64-123">OUTPUTS</span></span>

### <span data-ttu-id="d2d64-124">Ez a parancsmag nem hoz létre semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="d2d64-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="d2d64-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2d64-125">NOTES</span></span>

## <span data-ttu-id="d2d64-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2d64-126">RELATED LINKS</span></span>

[<span data-ttu-id="d2d64-127">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d2d64-127">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


