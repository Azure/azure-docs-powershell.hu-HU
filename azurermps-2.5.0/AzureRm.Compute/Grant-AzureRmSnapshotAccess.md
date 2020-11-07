---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermsnapshotaccess
schema: 2.0.0
ms.openlocfilehash: b1957543c959a18c9fd0fe4fc12de02064ffdcf0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849766"
---
# <span data-ttu-id="00b79-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="00b79-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="00b79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00b79-102">SYNOPSIS</span></span>
<span data-ttu-id="00b79-103">Hozzáférést ad egy pillanatképhez.</span><span class="sxs-lookup"><span data-stu-id="00b79-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00b79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00b79-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00b79-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="00b79-105">DESCRIPTION</span></span>
<span data-ttu-id="00b79-106">A **Grant-AzureRmSnapshotAccess** parancsmag hozzáférést ad egy pillanatképhez.</span><span class="sxs-lookup"><span data-stu-id="00b79-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="00b79-107">Példák</span><span class="sxs-lookup"><span data-stu-id="00b79-107">EXAMPLES</span></span>

### <span data-ttu-id="00b79-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="00b79-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="00b79-109">Adjon "READ" hozzáférést a "Snapshot01" nevű pillanatképhez a "ResourceGroup01" nevű erőforrás-csoportban, 60 másodperc múlva.</span><span class="sxs-lookup"><span data-stu-id="00b79-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="00b79-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00b79-110">PARAMETERS</span></span>

### <span data-ttu-id="00b79-111">-Access</span><span class="sxs-lookup"><span data-stu-id="00b79-111">-Access</span></span>
<span data-ttu-id="00b79-112">Hozzáférési szint megadása</span><span class="sxs-lookup"><span data-stu-id="00b79-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00b79-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00b79-113">-AsJob</span></span>
<span data-ttu-id="00b79-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="00b79-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00b79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b79-115">-DefaultProfile</span></span>
<span data-ttu-id="00b79-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00b79-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00b79-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="00b79-117">-DurationInSecond</span></span>
<span data-ttu-id="00b79-118">A hozzáférési időtartamot másodpercben adja meg.</span><span class="sxs-lookup"><span data-stu-id="00b79-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="00b79-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00b79-119">-ResourceGroupName</span></span>
<span data-ttu-id="00b79-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="00b79-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="00b79-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="00b79-121">-SnapshotName</span></span>
<span data-ttu-id="00b79-122">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="00b79-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="00b79-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="00b79-123">-Confirm</span></span>
<span data-ttu-id="00b79-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="00b79-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00b79-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00b79-125">-WhatIf</span></span>
<span data-ttu-id="00b79-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="00b79-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00b79-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00b79-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00b79-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b79-128">CommonParameters</span></span>
<span data-ttu-id="00b79-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00b79-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b79-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00b79-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b79-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00b79-131">INPUTS</span></span>

### <span data-ttu-id="00b79-132">System. String</span><span class="sxs-lookup"><span data-stu-id="00b79-132">System.String</span></span>

## <span data-ttu-id="00b79-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00b79-133">OUTPUTS</span></span>

### <span data-ttu-id="00b79-134">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="00b79-134">System.Object</span></span>

## <span data-ttu-id="00b79-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00b79-135">NOTES</span></span>

## <span data-ttu-id="00b79-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00b79-136">RELATED LINKS</span></span>

