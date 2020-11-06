---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: 2787c1cf8a37fd5d143e95c55d3e98b625d4d82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493194"
---
# <span data-ttu-id="36ba4-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="36ba4-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="36ba4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="36ba4-103">Hozzáférést biztosít a lemezhez.</span><span class="sxs-lookup"><span data-stu-id="36ba4-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36ba4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36ba4-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ba4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36ba4-105">DESCRIPTION</span></span>
<span data-ttu-id="36ba4-106">A **Grant-AzureRmDiskAccess** parancsmag hozzáférést biztosít a lemezhez.</span><span class="sxs-lookup"><span data-stu-id="36ba4-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="36ba4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="36ba4-107">EXAMPLES</span></span>

### <span data-ttu-id="36ba4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="36ba4-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="36ba4-109">Adjon "READ" hozzáférést a "ResourceGroup01" nevű erőforráscsoport "Disk01" nevű lemezéhez a 60-as másodpercben.</span><span class="sxs-lookup"><span data-stu-id="36ba4-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="36ba4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36ba4-110">PARAMETERS</span></span>

### <span data-ttu-id="36ba4-111">-Access</span><span class="sxs-lookup"><span data-stu-id="36ba4-111">-Access</span></span>
<span data-ttu-id="36ba4-112">Hozzáférési szint megadása</span><span class="sxs-lookup"><span data-stu-id="36ba4-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="36ba4-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="36ba4-113">-DiskName</span></span>
<span data-ttu-id="36ba4-114">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36ba4-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="36ba4-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="36ba4-115">-DurationInSecond</span></span>
<span data-ttu-id="36ba4-116">A hozzáférési időtartamot másodpercben adja meg.</span><span class="sxs-lookup"><span data-stu-id="36ba4-116">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="36ba4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ba4-117">-ResourceGroupName</span></span>
<span data-ttu-id="36ba4-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36ba4-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="36ba4-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36ba4-119">-Confirm</span></span>
<span data-ttu-id="36ba4-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36ba4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ba4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ba4-121">-WhatIf</span></span>
<span data-ttu-id="36ba4-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36ba4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36ba4-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36ba4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36ba4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ba4-124">CommonParameters</span></span>
<span data-ttu-id="36ba4-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36ba4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ba4-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ba4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ba4-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36ba4-127">INPUTS</span></span>

### <span data-ttu-id="36ba4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="36ba4-128">System.String</span></span>

## <span data-ttu-id="36ba4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36ba4-129">OUTPUTS</span></span>

### <span data-ttu-id="36ba4-130">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="36ba4-130">System.Object</span></span>

## <span data-ttu-id="36ba4-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36ba4-131">NOTES</span></span>

## <span data-ttu-id="36ba4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36ba4-132">RELATED LINKS</span></span>

