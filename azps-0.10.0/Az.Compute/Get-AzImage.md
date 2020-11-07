---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 13829081952be7ab79c6d7badde4dc687aa845ed
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844645"
---
# <span data-ttu-id="a2118-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="a2118-101">Get-AzImage</span></span>

## <span data-ttu-id="a2118-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2118-102">SYNOPSIS</span></span>
<span data-ttu-id="a2118-103">A kép tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="a2118-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="a2118-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2118-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2118-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2118-105">DESCRIPTION</span></span>
<span data-ttu-id="a2118-106">A **Get-AzImage** parancsmag a kép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a2118-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="a2118-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a2118-107">EXAMPLES</span></span>

### <span data-ttu-id="a2118-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a2118-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="a2118-109">Ez a parancs a ' Image01 ' nevű kép tulajdonságait kapja meg a "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="a2118-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a2118-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="a2118-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="a2118-111">Ez a parancs a "ResourceGroup01" erőforráscsoport összes képének tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2118-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a2118-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="a2118-112">Example 3</span></span>
```
PS C:\> Get-AzImage
```

<span data-ttu-id="a2118-113">Ez a parancs az előfizetés alatti képek tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a2118-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="a2118-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2118-114">PARAMETERS</span></span>

### <span data-ttu-id="a2118-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2118-115">-DefaultProfile</span></span>
<span data-ttu-id="a2118-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2118-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2118-117">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="a2118-117">-Expand</span></span>
<span data-ttu-id="a2118-118">A kifejezés kibontása lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2118-118">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="a2118-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="a2118-119">-ImageName</span></span>
<span data-ttu-id="a2118-120">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2118-120">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="a2118-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2118-121">-ResourceGroupName</span></span>
<span data-ttu-id="a2118-122">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2118-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a2118-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2118-123">CommonParameters</span></span>
<span data-ttu-id="a2118-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2118-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2118-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2118-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2118-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2118-126">INPUTS</span></span>

### <span data-ttu-id="a2118-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a2118-127">System.String</span></span>

## <span data-ttu-id="a2118-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2118-128">OUTPUTS</span></span>

### <span data-ttu-id="a2118-129">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="a2118-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="a2118-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2118-130">NOTES</span></span>

## <span data-ttu-id="a2118-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2118-131">RELATED LINKS</span></span>

