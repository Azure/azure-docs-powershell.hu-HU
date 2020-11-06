---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 2b9573e3add842478977cf620873d3cf0cfdaa8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503836"
---
# <span data-ttu-id="59579-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="59579-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="59579-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59579-102">SYNOPSIS</span></span>
<span data-ttu-id="59579-103">Hozzáférés visszavonása a lemezhez</span><span class="sxs-lookup"><span data-stu-id="59579-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59579-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59579-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59579-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59579-105">DESCRIPTION</span></span>
<span data-ttu-id="59579-106">A **Visszavonás-AzureRmDiskAccess** parancsmag visszavonja a lemezhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="59579-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="59579-107">Példák</span><span class="sxs-lookup"><span data-stu-id="59579-107">EXAMPLES</span></span>

### <span data-ttu-id="59579-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="59579-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="59579-109">A "ResourceGroup01" nevű erőforráscsoport "Disk01" nevű lemezéhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="59579-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="59579-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59579-110">PARAMETERS</span></span>

### <span data-ttu-id="59579-111">-DiskName</span><span class="sxs-lookup"><span data-stu-id="59579-111">-DiskName</span></span>
<span data-ttu-id="59579-112">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59579-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="59579-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59579-113">-ResourceGroupName</span></span>
<span data-ttu-id="59579-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59579-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="59579-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59579-115">-Confirm</span></span>
<span data-ttu-id="59579-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59579-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59579-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59579-117">-WhatIf</span></span>
<span data-ttu-id="59579-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59579-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59579-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59579-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59579-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59579-120">CommonParameters</span></span>
<span data-ttu-id="59579-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59579-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59579-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59579-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59579-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59579-123">INPUTS</span></span>

### <span data-ttu-id="59579-124">System. String</span><span class="sxs-lookup"><span data-stu-id="59579-124">System.String</span></span>

## <span data-ttu-id="59579-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59579-125">OUTPUTS</span></span>

### <span data-ttu-id="59579-126">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="59579-126">System.Object</span></span>

## <span data-ttu-id="59579-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59579-127">NOTES</span></span>

## <span data-ttu-id="59579-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59579-128">RELATED LINKS</span></span>

