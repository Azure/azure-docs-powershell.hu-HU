---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: d005f3f182109399f5a74b934959951dfb02c48e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844550"
---
# <span data-ttu-id="96db9-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="96db9-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="96db9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96db9-102">SYNOPSIS</span></span>
<span data-ttu-id="96db9-103">A VMSS elérhető SKU-ket kapja.</span><span class="sxs-lookup"><span data-stu-id="96db9-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="96db9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96db9-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96db9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96db9-105">DESCRIPTION</span></span>
<span data-ttu-id="96db9-106">A **Get-AzVmssSku** parancsmag a virtuálisgép-készlet (VMSS) számára elérhető SKU-ket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="96db9-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="96db9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="96db9-107">EXAMPLES</span></span>

### <span data-ttu-id="96db9-108">Példa 1: az összes elérhető SKU beszerzése a VMSS</span><span class="sxs-lookup"><span data-stu-id="96db9-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="96db9-109">Ez a parancs minden elérhető SKU-t beolvas a ContosoGroup nevű erőforráscsoport ContosoVMSS nevű VMSS.</span><span class="sxs-lookup"><span data-stu-id="96db9-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="96db9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96db9-110">PARAMETERS</span></span>

### <span data-ttu-id="96db9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96db9-111">-DefaultProfile</span></span>
<span data-ttu-id="96db9-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96db9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96db9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96db9-113">-ResourceGroupName</span></span>
<span data-ttu-id="96db9-114">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96db9-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="96db9-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="96db9-115">-VMScaleSetName</span></span>
<span data-ttu-id="96db9-116">Faj: a VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="96db9-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="96db9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96db9-117">CommonParameters</span></span>
<span data-ttu-id="96db9-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96db9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96db9-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96db9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96db9-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96db9-120">INPUTS</span></span>

### <span data-ttu-id="96db9-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="96db9-121">None</span></span>
<span data-ttu-id="96db9-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="96db9-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96db9-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96db9-123">OUTPUTS</span></span>

### <span data-ttu-id="96db9-124">Ez a parancsmag nem hoz létre semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="96db9-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="96db9-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96db9-125">NOTES</span></span>

## <span data-ttu-id="96db9-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96db9-126">RELATED LINKS</span></span>

[<span data-ttu-id="96db9-127">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="96db9-127">Get-AzVmss</span></span>](./Get-AzVmss.md)


