---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: 9b870214362c6e2bcd7225ef5a40ed5ff780139a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497116"
---
# <span data-ttu-id="5cd89-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="5cd89-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="5cd89-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5cd89-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd89-103">Hozzáférést ad egy pillanatképhez.</span><span class="sxs-lookup"><span data-stu-id="5cd89-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cd89-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5cd89-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5cd89-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5cd89-105">DESCRIPTION</span></span>
<span data-ttu-id="5cd89-106">A **Grant-AzureRmSnapshotAccess** parancsmag hozzáférést ad egy pillanatképhez.</span><span class="sxs-lookup"><span data-stu-id="5cd89-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="5cd89-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5cd89-107">EXAMPLES</span></span>

### <span data-ttu-id="5cd89-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5cd89-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="5cd89-109">Adjon "READ" hozzáférést a "Snapshot01" nevű pillanatképhez a "ResourceGroup01" nevű erőforrás-csoportban, 60 másodperc múlva.</span><span class="sxs-lookup"><span data-stu-id="5cd89-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="5cd89-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5cd89-110">PARAMETERS</span></span>

### <span data-ttu-id="5cd89-111">-Access</span><span class="sxs-lookup"><span data-stu-id="5cd89-111">-Access</span></span>
<span data-ttu-id="5cd89-112">Hozzáférési szint megadása</span><span class="sxs-lookup"><span data-stu-id="5cd89-112">Specifies Access level.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd89-113">-DefaultProfile</span></span>
<span data-ttu-id="5cd89-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5cd89-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cd89-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="5cd89-115">-DurationInSecond</span></span>
<span data-ttu-id="5cd89-116">A hozzáférési időtartamot másodpercben adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cd89-116">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd89-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd89-117">-ResourceGroupName</span></span>
<span data-ttu-id="5cd89-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cd89-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5cd89-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="5cd89-119">-SnapshotName</span></span>
<span data-ttu-id="5cd89-120">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5cd89-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="5cd89-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5cd89-121">-Confirm</span></span>
<span data-ttu-id="5cd89-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5cd89-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cd89-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cd89-123">-WhatIf</span></span>
<span data-ttu-id="5cd89-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5cd89-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cd89-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5cd89-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cd89-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd89-126">CommonParameters</span></span>
<span data-ttu-id="5cd89-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5cd89-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd89-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cd89-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd89-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cd89-129">INPUTS</span></span>

### <span data-ttu-id="5cd89-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5cd89-130">System.String</span></span>

## <span data-ttu-id="5cd89-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cd89-131">OUTPUTS</span></span>

### <span data-ttu-id="5cd89-132">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="5cd89-132">System.Object</span></span>

## <span data-ttu-id="5cd89-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5cd89-133">NOTES</span></span>

## <span data-ttu-id="5cd89-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cd89-134">RELATED LINKS</span></span>

