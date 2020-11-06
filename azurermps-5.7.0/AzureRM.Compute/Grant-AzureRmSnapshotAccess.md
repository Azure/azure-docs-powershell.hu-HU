---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: 8f68957020d8e4607477bd78cc42b05c29e321c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492380"
---
# <span data-ttu-id="a00b2-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a00b2-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="a00b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a00b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a00b2-103">Hozzáférést ad egy pillanatképhez.</span><span class="sxs-lookup"><span data-stu-id="a00b2-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a00b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a00b2-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a00b2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a00b2-105">DESCRIPTION</span></span>
<span data-ttu-id="a00b2-106">A **Grant-AzureRmSnapshotAccess** parancsmag hozzáférést ad egy pillanatképhez.</span><span class="sxs-lookup"><span data-stu-id="a00b2-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="a00b2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a00b2-107">EXAMPLES</span></span>

### <span data-ttu-id="a00b2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a00b2-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="a00b2-109">Adjon "READ" hozzáférést a "Snapshot01" nevű pillanatképhez a "ResourceGroup01" nevű erőforrás-csoportban, 60 másodperc múlva.</span><span class="sxs-lookup"><span data-stu-id="a00b2-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="a00b2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a00b2-110">PARAMETERS</span></span>

### <span data-ttu-id="a00b2-111">-Access</span><span class="sxs-lookup"><span data-stu-id="a00b2-111">-Access</span></span>
<span data-ttu-id="a00b2-112">Hozzáférési szint megadása</span><span class="sxs-lookup"><span data-stu-id="a00b2-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00b2-113">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="a00b2-113">-DurationInSecond</span></span>
<span data-ttu-id="a00b2-114">A hozzáférési időtartamot másodpercben adja meg.</span><span class="sxs-lookup"><span data-stu-id="a00b2-114">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00b2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a00b2-115">-ResourceGroupName</span></span>
<span data-ttu-id="a00b2-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a00b2-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a00b2-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="a00b2-117">-SnapshotName</span></span>
<span data-ttu-id="a00b2-118">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a00b2-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="a00b2-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a00b2-119">-Confirm</span></span>
<span data-ttu-id="a00b2-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a00b2-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00b2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a00b2-121">-WhatIf</span></span>
<span data-ttu-id="a00b2-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a00b2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a00b2-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a00b2-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a00b2-124">CommonParameters</span></span>
<span data-ttu-id="a00b2-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a00b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a00b2-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a00b2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a00b2-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a00b2-127">INPUTS</span></span>

### <span data-ttu-id="a00b2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a00b2-128">System.String</span></span>

## <span data-ttu-id="a00b2-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a00b2-129">OUTPUTS</span></span>

### <span data-ttu-id="a00b2-130">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="a00b2-130">System.Object</span></span>

## <span data-ttu-id="a00b2-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a00b2-131">NOTES</span></span>

## <span data-ttu-id="a00b2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a00b2-132">RELATED LINKS</span></span>

