---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermimage
schema: 2.0.0
ms.openlocfilehash: 8508a7353924342449324588e90abf3807d7f7ac
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849405"
---
# <span data-ttu-id="9181a-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="9181a-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="9181a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9181a-102">SYNOPSIS</span></span>
<span data-ttu-id="9181a-103">A kép tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="9181a-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9181a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9181a-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9181a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9181a-105">DESCRIPTION</span></span>
<span data-ttu-id="9181a-106">A **Get-AzureRmImage** parancsmag a kép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9181a-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="9181a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9181a-107">EXAMPLES</span></span>

### <span data-ttu-id="9181a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9181a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="9181a-109">Ez a parancs a ' Image01 ' nevű kép tulajdonságait kapja meg a "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="9181a-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="9181a-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="9181a-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="9181a-111">Ez a parancs a "ResourceGroup01" erőforráscsoport összes képének tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9181a-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="9181a-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="9181a-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="9181a-113">Ez a parancs az előfizetés alatti képek tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9181a-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="9181a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9181a-114">PARAMETERS</span></span>

### <span data-ttu-id="9181a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9181a-115">-DefaultProfile</span></span>
<span data-ttu-id="9181a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9181a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9181a-117">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="9181a-117">-Expand</span></span>
<span data-ttu-id="9181a-118">A kifejezés kibontása lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="9181a-118">Specifies the expand expression query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9181a-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="9181a-119">-ImageName</span></span>
<span data-ttu-id="9181a-120">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9181a-120">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9181a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9181a-121">-ResourceGroupName</span></span>
<span data-ttu-id="9181a-122">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9181a-122">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9181a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9181a-123">CommonParameters</span></span>
<span data-ttu-id="9181a-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9181a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9181a-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9181a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9181a-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9181a-126">INPUTS</span></span>

### <span data-ttu-id="9181a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9181a-127">System.String</span></span>

## <span data-ttu-id="9181a-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9181a-128">OUTPUTS</span></span>

### <span data-ttu-id="9181a-129">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="9181a-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="9181a-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9181a-130">NOTES</span></span>

## <span data-ttu-id="9181a-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9181a-131">RELATED LINKS</span></span>

