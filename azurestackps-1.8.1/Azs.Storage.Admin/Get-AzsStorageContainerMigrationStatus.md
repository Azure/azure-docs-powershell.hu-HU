---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96220d7bac0a71f579f81a4d01f4f1dc3cba9dd1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840661"
---
# <span data-ttu-id="1091c-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="1091c-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="1091c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1091c-102">SYNOPSIS</span></span>
<span data-ttu-id="1091c-103">Egy tároló áttelepítési feladatának állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="1091c-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="1091c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1091c-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="1091c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1091c-105">DESCRIPTION</span></span>
<span data-ttu-id="1091c-106">Egy tároló áttelepítési feladatának állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="1091c-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="1091c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1091c-107">EXAMPLES</span></span>

### <span data-ttu-id="1091c-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="1091c-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="1091c-109">Adattároló áttelepítési feladat állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="1091c-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="1091c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1091c-110">PARAMETERS</span></span>

### <span data-ttu-id="1091c-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="1091c-111">-FarmName</span></span>
<span data-ttu-id="1091c-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="1091c-112">Farm Id.</span></span>

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

### <span data-ttu-id="1091c-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="1091c-113">-JobId</span></span>
<span data-ttu-id="1091c-114">Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="1091c-114">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1091c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1091c-115">-ResourceGroupName</span></span>
<span data-ttu-id="1091c-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1091c-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1091c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1091c-117">CommonParameters</span></span>
<span data-ttu-id="1091c-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1091c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1091c-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1091c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1091c-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1091c-120">INPUTS</span></span>

## <span data-ttu-id="1091c-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1091c-121">OUTPUTS</span></span>

### <span data-ttu-id="1091c-122">Microsoft. AzureStack. Management. Storage. admin. models. MigrationResult</span><span class="sxs-lookup"><span data-stu-id="1091c-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="1091c-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1091c-123">NOTES</span></span>

## <span data-ttu-id="1091c-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1091c-124">RELATED LINKS</span></span>
