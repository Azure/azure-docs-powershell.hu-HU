---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 36dec1f8d4374f2e5bbed1f742aa7733bb760f67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495439"
---
# <span data-ttu-id="4825f-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="4825f-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="4825f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4825f-102">SYNOPSIS</span></span>
<span data-ttu-id="4825f-103">Pillanatkép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4825f-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4825f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4825f-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4825f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4825f-105">DESCRIPTION</span></span>
<span data-ttu-id="4825f-106">A **Remove-AzureRmSnapshot** parancsmag eltávolítja a pillanatképet.</span><span class="sxs-lookup"><span data-stu-id="4825f-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="4825f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4825f-107">EXAMPLES</span></span>

### <span data-ttu-id="4825f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4825f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="4825f-109">Ez a parancs eltávolítja a "Snapshot01" nevű pillanatképet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="4825f-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4825f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4825f-110">PARAMETERS</span></span>

### <span data-ttu-id="4825f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4825f-111">-Force</span></span>
<span data-ttu-id="4825f-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4825f-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4825f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4825f-113">-ResourceGroupName</span></span>
<span data-ttu-id="4825f-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4825f-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4825f-115">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="4825f-115">-SnapshotName</span></span>
<span data-ttu-id="4825f-116">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4825f-116">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="4825f-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4825f-117">-Confirm</span></span>
<span data-ttu-id="4825f-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4825f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4825f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4825f-119">-WhatIf</span></span>
<span data-ttu-id="4825f-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4825f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4825f-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4825f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4825f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4825f-122">CommonParameters</span></span>
<span data-ttu-id="4825f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4825f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4825f-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4825f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4825f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4825f-125">INPUTS</span></span>

### <span data-ttu-id="4825f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4825f-126">System.String</span></span>

## <span data-ttu-id="4825f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4825f-127">OUTPUTS</span></span>

### <span data-ttu-id="4825f-128">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="4825f-128">System.Object</span></span>

## <span data-ttu-id="4825f-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4825f-129">NOTES</span></span>

## <span data-ttu-id="4825f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4825f-130">RELATED LINKS</span></span>

