---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: 3976418d89076b290500343775ca42e2fb975659
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497732"
---
# <span data-ttu-id="8b8c5-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="8b8c5-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="8b8c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b8c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8b8c5-103">A kép tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="8b8c5-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b8c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b8c5-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b8c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b8c5-105">DESCRIPTION</span></span>
<span data-ttu-id="8b8c5-106">A **Get-AzureRmImage** parancsmag a kép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8b8c5-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="8b8c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8b8c5-107">EXAMPLES</span></span>

### <span data-ttu-id="8b8c5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8b8c5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="8b8c5-109">Ez a parancs a ' Image01 ' nevű kép tulajdonságait kapja meg a "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="8b8c5-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="8b8c5-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="8b8c5-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="8b8c5-111">Ez a parancs a "ResourceGroup01" erőforráscsoport összes képének tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b8c5-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="8b8c5-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="8b8c5-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="8b8c5-113">Ez a parancs az előfizetés alatti képek tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8b8c5-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="8b8c5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b8c5-114">PARAMETERS</span></span>

### <span data-ttu-id="8b8c5-115">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="8b8c5-115">-Expand</span></span>
<span data-ttu-id="8b8c5-116">A kifejezés kibontása lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b8c5-116">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="8b8c5-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="8b8c5-117">-ImageName</span></span>
<span data-ttu-id="8b8c5-118">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b8c5-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="8b8c5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b8c5-119">-ResourceGroupName</span></span>
<span data-ttu-id="8b8c5-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b8c5-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8b8c5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b8c5-121">CommonParameters</span></span>
<span data-ttu-id="8b8c5-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b8c5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b8c5-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b8c5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b8c5-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b8c5-124">INPUTS</span></span>

### <span data-ttu-id="8b8c5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8b8c5-125">System.String</span></span>

## <span data-ttu-id="8b8c5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b8c5-126">OUTPUTS</span></span>

### <span data-ttu-id="8b8c5-127">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="8b8c5-127">System.Object</span></span>

## <span data-ttu-id="8b8c5-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b8c5-128">NOTES</span></span>

## <span data-ttu-id="8b8c5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b8c5-129">RELATED LINKS</span></span>

