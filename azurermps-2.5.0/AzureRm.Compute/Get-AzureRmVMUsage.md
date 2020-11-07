---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
ms.openlocfilehash: 210c66f91836b40c719d91907fc78bd907d0fe86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850930"
---
# <span data-ttu-id="78dc0-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="78dc0-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="78dc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="78dc0-103">Beilleszti a virtuális gép alapvető számát a helyhez.</span><span class="sxs-lookup"><span data-stu-id="78dc0-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78dc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78dc0-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78dc0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="78dc0-105">DESCRIPTION</span></span>
<span data-ttu-id="78dc0-106">A **Get-AzureRmVMUsage** parancsmag a Virtual Machine Core Count használatát kapja meg egy helyhez.</span><span class="sxs-lookup"><span data-stu-id="78dc0-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="78dc0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="78dc0-107">EXAMPLES</span></span>

### <span data-ttu-id="78dc0-108">Példa 1: egy hely alapvető számlálási használati területének beszerzése</span><span class="sxs-lookup"><span data-stu-id="78dc0-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="78dc0-109">Ez a parancs a Virtual Machine Core Count használatát a közép-amerikai helyhez kapja.</span><span class="sxs-lookup"><span data-stu-id="78dc0-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="78dc0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78dc0-110">PARAMETERS</span></span>

### <span data-ttu-id="78dc0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78dc0-111">-DefaultProfile</span></span>
<span data-ttu-id="78dc0-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78dc0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78dc0-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="78dc0-113">-Location</span></span>
<span data-ttu-id="78dc0-114">Azt a helyet adja meg, ahol ez a parancsmag a Virtual Machine Core Count használatát kapja.</span><span class="sxs-lookup"><span data-stu-id="78dc0-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="78dc0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78dc0-115">CommonParameters</span></span>
<span data-ttu-id="78dc0-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78dc0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78dc0-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78dc0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78dc0-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78dc0-118">INPUTS</span></span>

### <span data-ttu-id="78dc0-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="78dc0-119">None</span></span>
<span data-ttu-id="78dc0-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="78dc0-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="78dc0-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78dc0-121">OUTPUTS</span></span>

### <span data-ttu-id="78dc0-122">Microsoft. Azure. commands. kiszámítás. modellek. PSUs</span><span class="sxs-lookup"><span data-stu-id="78dc0-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="78dc0-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78dc0-123">NOTES</span></span>

## <span data-ttu-id="78dc0-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78dc0-124">RELATED LINKS</span></span>

[<span data-ttu-id="78dc0-125">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="78dc0-125">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


