---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cc6e2adff73e4b7c81a401bb98e9ab625005ae3f
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840274"
---
# <span data-ttu-id="97a19-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="97a19-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="97a19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97a19-102">SYNOPSIS</span></span>
<span data-ttu-id="97a19-103">A tárterület-megosztások listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="97a19-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="97a19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97a19-104">SYNTAX</span></span>

### <span data-ttu-id="97a19-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97a19-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="97a19-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="97a19-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="97a19-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="97a19-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="97a19-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="97a19-108">DESCRIPTION</span></span>
<span data-ttu-id="97a19-109">A tárterület-megosztások listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="97a19-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="97a19-110">Példák</span><span class="sxs-lookup"><span data-stu-id="97a19-110">EXAMPLES</span></span>

### <span data-ttu-id="97a19-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="97a19-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="97a19-112">A tárterület-megosztások listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="97a19-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="97a19-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97a19-113">PARAMETERS</span></span>

### <span data-ttu-id="97a19-114">-FarmName</span><span class="sxs-lookup"><span data-stu-id="97a19-114">-FarmName</span></span>
<span data-ttu-id="97a19-115">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="97a19-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a19-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97a19-116">-Name</span></span>
<span data-ttu-id="97a19-117">Megosztási név.</span><span class="sxs-lookup"><span data-stu-id="97a19-117">Share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a19-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97a19-118">-ResourceGroupName</span></span>
<span data-ttu-id="97a19-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="97a19-119">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a19-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97a19-120">-ResourceId</span></span>
<span data-ttu-id="97a19-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="97a19-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a19-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a19-122">CommonParameters</span></span>
<span data-ttu-id="97a19-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97a19-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a19-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97a19-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a19-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97a19-125">INPUTS</span></span>

## <span data-ttu-id="97a19-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97a19-126">OUTPUTS</span></span>

### <span data-ttu-id="97a19-127">Microsoft. AzureStack. Management. Storage. admin. models. share</span><span class="sxs-lookup"><span data-stu-id="97a19-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="97a19-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97a19-128">NOTES</span></span>

## <span data-ttu-id="97a19-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97a19-129">RELATED LINKS</span></span>

