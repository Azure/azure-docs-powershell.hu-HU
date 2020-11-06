---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 4c7260d3c1131ab573bf933f4b83022cef20819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505148"
---
# <span data-ttu-id="6b801-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="6b801-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="6b801-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b801-102">SYNOPSIS</span></span>
<span data-ttu-id="6b801-103">Pillanatkép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6b801-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b801-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b801-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b801-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b801-105">DESCRIPTION</span></span>
<span data-ttu-id="6b801-106">A **Remove-AzureRmSnapshot** parancsmag eltávolítja a pillanatképet.</span><span class="sxs-lookup"><span data-stu-id="6b801-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="6b801-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6b801-107">EXAMPLES</span></span>

### <span data-ttu-id="6b801-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6b801-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="6b801-109">Ez a parancs eltávolítja a "Snapshot01" nevű pillanatképet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="6b801-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6b801-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b801-110">PARAMETERS</span></span>

### <span data-ttu-id="6b801-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b801-111">-DefaultProfile</span></span>
<span data-ttu-id="6b801-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b801-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b801-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6b801-113">-Force</span></span>
<span data-ttu-id="6b801-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6b801-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b801-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b801-115">-ResourceGroupName</span></span>
<span data-ttu-id="6b801-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b801-116">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b801-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="6b801-117">-SnapshotName</span></span>
<span data-ttu-id="6b801-118">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b801-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b801-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6b801-119">-Confirm</span></span>
<span data-ttu-id="6b801-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6b801-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b801-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b801-121">-WhatIf</span></span>
<span data-ttu-id="6b801-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6b801-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b801-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b801-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b801-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b801-124">CommonParameters</span></span>
<span data-ttu-id="6b801-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b801-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b801-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b801-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b801-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b801-127">INPUTS</span></span>

### <span data-ttu-id="6b801-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6b801-128">System.String</span></span>

## <span data-ttu-id="6b801-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b801-129">OUTPUTS</span></span>

### <span data-ttu-id="6b801-130">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="6b801-130">System.Object</span></span>

## <span data-ttu-id="6b801-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b801-131">NOTES</span></span>

## <span data-ttu-id="6b801-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b801-132">RELATED LINKS</span></span>

