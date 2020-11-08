---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0fb6da4bde577d5a69c5bd85261822e3cf1865d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016903"
---
# <span data-ttu-id="aba1b-101">Get-AzsBlobService</span><span class="sxs-lookup"><span data-stu-id="aba1b-101">Get-AzsBlobService</span></span>

## <span data-ttu-id="aba1b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aba1b-102">SYNOPSIS</span></span>
<span data-ttu-id="aba1b-103">A blob-szolgáltatás értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="aba1b-103">Returns the blob service.</span></span>

## <span data-ttu-id="aba1b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aba1b-104">SYNTAX</span></span>

```
Get-AzsBlobService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="aba1b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aba1b-105">DESCRIPTION</span></span>
<span data-ttu-id="aba1b-106">A blob-szolgáltatás értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="aba1b-106">Returns the blob service.</span></span>

## <span data-ttu-id="aba1b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aba1b-107">EXAMPLES</span></span>

### <span data-ttu-id="aba1b-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="aba1b-108">EXAMPLE 1</span></span>
```
Get-AzsBlobService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="aba1b-109">A Paca szolgáltatás beszerzése.</span><span class="sxs-lookup"><span data-stu-id="aba1b-109">Get the blob service.</span></span>

## <span data-ttu-id="aba1b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aba1b-110">PARAMETERS</span></span>

### <span data-ttu-id="aba1b-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="aba1b-111">-FarmName</span></span>
<span data-ttu-id="aba1b-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="aba1b-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba1b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aba1b-113">-ResourceGroupName</span></span>
<span data-ttu-id="aba1b-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="aba1b-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba1b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba1b-115">CommonParameters</span></span>
<span data-ttu-id="aba1b-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aba1b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba1b-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aba1b-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba1b-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aba1b-118">INPUTS</span></span>

## <span data-ttu-id="aba1b-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aba1b-119">OUTPUTS</span></span>

### <span data-ttu-id="aba1b-120">Microsoft. AzureStack. Management. Storage. admin. models. BlobService</span><span class="sxs-lookup"><span data-stu-id="aba1b-120">Microsoft.AzureStack.Management.Storage.Admin.Models.BlobService</span></span>

## <span data-ttu-id="aba1b-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aba1b-121">NOTES</span></span>

## <span data-ttu-id="aba1b-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aba1b-122">RELATED LINKS</span></span>
