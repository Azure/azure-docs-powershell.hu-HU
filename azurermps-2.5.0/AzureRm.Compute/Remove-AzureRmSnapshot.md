---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: cf63923b278f009cb676c79642882e64e6b8e303
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850066"
---
# <span data-ttu-id="395c9-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="395c9-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="395c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="395c9-102">SYNOPSIS</span></span>
<span data-ttu-id="395c9-103">Pillanatkép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="395c9-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="395c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="395c9-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="395c9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="395c9-105">DESCRIPTION</span></span>
<span data-ttu-id="395c9-106">A **Remove-AzureRmSnapshot** parancsmag eltávolítja a pillanatképet.</span><span class="sxs-lookup"><span data-stu-id="395c9-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="395c9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="395c9-107">EXAMPLES</span></span>

### <span data-ttu-id="395c9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="395c9-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="395c9-109">Ez a parancs eltávolítja a "Snapshot01" nevű pillanatképet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="395c9-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="395c9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="395c9-110">PARAMETERS</span></span>

### <span data-ttu-id="395c9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="395c9-111">-AsJob</span></span>
<span data-ttu-id="395c9-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="395c9-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395c9-113">-DefaultProfile</span></span>
<span data-ttu-id="395c9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="395c9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="395c9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="395c9-115">-Force</span></span>
<span data-ttu-id="395c9-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="395c9-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395c9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="395c9-117">-ResourceGroupName</span></span>
<span data-ttu-id="395c9-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="395c9-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="395c9-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="395c9-119">-SnapshotName</span></span>
<span data-ttu-id="395c9-120">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="395c9-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="395c9-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="395c9-121">-Confirm</span></span>
<span data-ttu-id="395c9-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="395c9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="395c9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="395c9-123">-WhatIf</span></span>
<span data-ttu-id="395c9-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="395c9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="395c9-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="395c9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="395c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395c9-126">CommonParameters</span></span>
<span data-ttu-id="395c9-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="395c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395c9-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="395c9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395c9-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="395c9-129">INPUTS</span></span>

### <span data-ttu-id="395c9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="395c9-130">System.String</span></span>

## <span data-ttu-id="395c9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="395c9-131">OUTPUTS</span></span>

### <span data-ttu-id="395c9-132">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="395c9-132">System.Object</span></span>

## <span data-ttu-id="395c9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="395c9-133">NOTES</span></span>

## <span data-ttu-id="395c9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="395c9-134">RELATED LINKS</span></span>

