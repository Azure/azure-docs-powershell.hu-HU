---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: f8da805a2c15356a4bf2188238b9a42a10617427
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848882"
---
# <span data-ttu-id="c6464-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c6464-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="c6464-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6464-102">SYNOPSIS</span></span>
<span data-ttu-id="c6464-103">Hozzáférés visszavonása a lemezhez</span><span class="sxs-lookup"><span data-stu-id="c6464-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6464-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6464-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6464-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6464-105">DESCRIPTION</span></span>
<span data-ttu-id="c6464-106">A **Visszavonás-AzureRmDiskAccess** parancsmag visszavonja a lemezhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="c6464-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="c6464-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c6464-107">EXAMPLES</span></span>

### <span data-ttu-id="c6464-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c6464-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="c6464-109">A "ResourceGroup01" nevű erőforráscsoport "Disk01" nevű lemezéhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="c6464-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="c6464-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6464-110">PARAMETERS</span></span>

### <span data-ttu-id="c6464-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6464-111">-AsJob</span></span>
<span data-ttu-id="c6464-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c6464-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6464-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6464-113">-DefaultProfile</span></span>
<span data-ttu-id="c6464-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6464-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6464-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="c6464-115">-DiskName</span></span>
<span data-ttu-id="c6464-116">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6464-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="c6464-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6464-117">-ResourceGroupName</span></span>
<span data-ttu-id="c6464-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6464-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c6464-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c6464-119">-Confirm</span></span>
<span data-ttu-id="c6464-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c6464-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6464-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6464-121">-WhatIf</span></span>
<span data-ttu-id="c6464-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c6464-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6464-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6464-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6464-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6464-124">CommonParameters</span></span>
<span data-ttu-id="c6464-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6464-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6464-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6464-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6464-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6464-127">INPUTS</span></span>

### <span data-ttu-id="c6464-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c6464-128">System.String</span></span>

## <span data-ttu-id="c6464-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6464-129">OUTPUTS</span></span>

### <span data-ttu-id="c6464-130">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="c6464-130">System.Object</span></span>

## <span data-ttu-id="c6464-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6464-131">NOTES</span></span>

## <span data-ttu-id="c6464-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6464-132">RELATED LINKS</span></span>

