---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: d081218a17bd5cac99256918d40ece722b73a85b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680178"
---
# <span data-ttu-id="ab52f-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ab52f-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="ab52f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab52f-102">SYNOPSIS</span></span>
<span data-ttu-id="ab52f-103">A pillanatképhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="ab52f-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab52f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab52f-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab52f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab52f-105">DESCRIPTION</span></span>
<span data-ttu-id="ab52f-106">A **Visszavonás-AzureRmSnapshotAccess** parancsmag visszavonja a pillanatképhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="ab52f-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="ab52f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ab52f-107">EXAMPLES</span></span>

### <span data-ttu-id="ab52f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ab52f-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="ab52f-109">A "ResourceGroup01" nevű erőforráscsoport "Snapshot01" nevű pillanatképéhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="ab52f-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="ab52f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab52f-110">PARAMETERS</span></span>

### <span data-ttu-id="ab52f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab52f-111">-ResourceGroupName</span></span>
<span data-ttu-id="ab52f-112">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab52f-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ab52f-113">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="ab52f-113">-SnapshotName</span></span>
<span data-ttu-id="ab52f-114">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab52f-114">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="ab52f-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ab52f-115">-Confirm</span></span>
<span data-ttu-id="ab52f-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ab52f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab52f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab52f-117">-WhatIf</span></span>
<span data-ttu-id="ab52f-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ab52f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab52f-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ab52f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab52f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab52f-120">CommonParameters</span></span>
<span data-ttu-id="ab52f-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab52f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab52f-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab52f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab52f-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab52f-123">INPUTS</span></span>

### <span data-ttu-id="ab52f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ab52f-124">System.String</span></span>

## <span data-ttu-id="ab52f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab52f-125">OUTPUTS</span></span>

### <span data-ttu-id="ab52f-126">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="ab52f-126">System.Object</span></span>

## <span data-ttu-id="ab52f-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab52f-127">NOTES</span></span>

## <span data-ttu-id="ab52f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab52f-128">RELATED LINKS</span></span>

