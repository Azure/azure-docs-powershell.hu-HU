---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 66a74ed2fa389c0dd39fa9fc86570ff8d68dc1dc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844554"
---
# <span data-ttu-id="d41bd-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="d41bd-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="d41bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d41bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d41bd-103">Beilleszti a virtuális gép alapvető számát a helyhez.</span><span class="sxs-lookup"><span data-stu-id="d41bd-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="d41bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d41bd-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d41bd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d41bd-105">DESCRIPTION</span></span>
<span data-ttu-id="d41bd-106">A **Get-AzVMUsage** parancsmag a Virtual Machine Core Count használatát kapja meg egy helyhez.</span><span class="sxs-lookup"><span data-stu-id="d41bd-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="d41bd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d41bd-107">EXAMPLES</span></span>

### <span data-ttu-id="d41bd-108">Példa 1: egy hely alapvető számlálási használati területének beszerzése</span><span class="sxs-lookup"><span data-stu-id="d41bd-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="d41bd-109">Ez a parancs a Virtual Machine Core Count használatát a közép-amerikai helyhez kapja.</span><span class="sxs-lookup"><span data-stu-id="d41bd-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="d41bd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d41bd-110">PARAMETERS</span></span>

### <span data-ttu-id="d41bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d41bd-111">-DefaultProfile</span></span>
<span data-ttu-id="d41bd-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d41bd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d41bd-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="d41bd-113">-Location</span></span>
<span data-ttu-id="d41bd-114">Azt a helyet adja meg, ahol ez a parancsmag a Virtual Machine Core Count használatát kapja.</span><span class="sxs-lookup"><span data-stu-id="d41bd-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="d41bd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d41bd-115">CommonParameters</span></span>
<span data-ttu-id="d41bd-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d41bd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d41bd-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d41bd-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d41bd-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d41bd-118">INPUTS</span></span>

### <span data-ttu-id="d41bd-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="d41bd-119">None</span></span>
<span data-ttu-id="d41bd-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d41bd-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d41bd-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d41bd-121">OUTPUTS</span></span>

### <span data-ttu-id="d41bd-122">Microsoft. Azure. commands. kiszámítás. modellek. PSUs</span><span class="sxs-lookup"><span data-stu-id="d41bd-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="d41bd-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d41bd-123">NOTES</span></span>

## <span data-ttu-id="d41bd-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d41bd-124">RELATED LINKS</span></span>

[<span data-ttu-id="d41bd-125">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d41bd-125">Get-AzVM</span></span>](./Get-AzVM.md)


