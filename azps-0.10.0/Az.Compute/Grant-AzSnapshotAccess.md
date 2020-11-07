---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: e4283b23fb4a82c17f35354d854c30c3ec1b2329
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844521"
---
# <span data-ttu-id="7b124-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="7b124-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="7b124-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b124-102">SYNOPSIS</span></span>
<span data-ttu-id="7b124-103">Hozzáférést ad egy pillanatképhez.</span><span class="sxs-lookup"><span data-stu-id="7b124-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="7b124-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b124-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b124-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b124-105">DESCRIPTION</span></span>
<span data-ttu-id="7b124-106">A **Grant-AzSnapshotAccess** parancsmag hozzáférést ad egy pillanatképhez.</span><span class="sxs-lookup"><span data-stu-id="7b124-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="7b124-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7b124-107">EXAMPLES</span></span>

### <span data-ttu-id="7b124-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7b124-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="7b124-109">Adjon "READ" hozzáférést a "Snapshot01" nevű pillanatképhez a "ResourceGroup01" nevű erőforrás-csoportban, 60 másodperc múlva.</span><span class="sxs-lookup"><span data-stu-id="7b124-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="7b124-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b124-110">PARAMETERS</span></span>

### <span data-ttu-id="7b124-111">-Access</span><span class="sxs-lookup"><span data-stu-id="7b124-111">-Access</span></span>
<span data-ttu-id="7b124-112">Hozzáférési szint megadása</span><span class="sxs-lookup"><span data-stu-id="7b124-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="7b124-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b124-113">-AsJob</span></span>
<span data-ttu-id="7b124-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7b124-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b124-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b124-115">-DefaultProfile</span></span>
<span data-ttu-id="7b124-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b124-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b124-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="7b124-117">-DurationInSecond</span></span>
<span data-ttu-id="7b124-118">A hozzáférési időtartamot másodpercben adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b124-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="7b124-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b124-119">-ResourceGroupName</span></span>
<span data-ttu-id="7b124-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b124-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7b124-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="7b124-121">-SnapshotName</span></span>
<span data-ttu-id="7b124-122">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b124-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="7b124-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7b124-123">-Confirm</span></span>
<span data-ttu-id="7b124-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7b124-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b124-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b124-125">-WhatIf</span></span>
<span data-ttu-id="7b124-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7b124-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b124-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b124-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b124-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b124-128">CommonParameters</span></span>
<span data-ttu-id="7b124-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b124-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b124-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b124-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b124-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b124-131">INPUTS</span></span>

### <span data-ttu-id="7b124-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7b124-132">System.String</span></span>

## <span data-ttu-id="7b124-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b124-133">OUTPUTS</span></span>

### <span data-ttu-id="7b124-134">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="7b124-134">System.Object</span></span>

## <span data-ttu-id="7b124-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b124-135">NOTES</span></span>

## <span data-ttu-id="7b124-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b124-136">RELATED LINKS</span></span>

