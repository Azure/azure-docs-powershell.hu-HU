---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
ms.openlocfilehash: bbde391c56d4b50320f15441b75b93d125771ccb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850913"
---
# <span data-ttu-id="9e741-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="9e741-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="9e741-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e741-102">SYNOPSIS</span></span>
<span data-ttu-id="9e741-103">A pillanatképhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="9e741-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e741-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e741-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e741-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e741-105">DESCRIPTION</span></span>
<span data-ttu-id="9e741-106">A **Visszavonás-AzureRmSnapshotAccess** parancsmag visszavonja a pillanatképhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="9e741-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="9e741-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9e741-107">EXAMPLES</span></span>

### <span data-ttu-id="9e741-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9e741-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="9e741-109">A "ResourceGroup01" nevű erőforráscsoport "Snapshot01" nevű pillanatképéhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="9e741-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="9e741-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e741-110">PARAMETERS</span></span>

### <span data-ttu-id="9e741-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e741-111">-AsJob</span></span>
<span data-ttu-id="9e741-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9e741-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e741-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e741-113">-DefaultProfile</span></span>
<span data-ttu-id="9e741-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e741-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e741-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e741-115">-ResourceGroupName</span></span>
<span data-ttu-id="9e741-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e741-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9e741-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="9e741-117">-SnapshotName</span></span>
<span data-ttu-id="9e741-118">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e741-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="9e741-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9e741-119">-Confirm</span></span>
<span data-ttu-id="9e741-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9e741-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e741-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e741-121">-WhatIf</span></span>
<span data-ttu-id="9e741-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9e741-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e741-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e741-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e741-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e741-124">CommonParameters</span></span>
<span data-ttu-id="9e741-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e741-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e741-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e741-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e741-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e741-127">INPUTS</span></span>

### <span data-ttu-id="9e741-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9e741-128">System.String</span></span>

## <span data-ttu-id="9e741-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e741-129">OUTPUTS</span></span>

### <span data-ttu-id="9e741-130">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="9e741-130">System.Object</span></span>

## <span data-ttu-id="9e741-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e741-131">NOTES</span></span>

## <span data-ttu-id="9e741-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e741-132">RELATED LINKS</span></span>

