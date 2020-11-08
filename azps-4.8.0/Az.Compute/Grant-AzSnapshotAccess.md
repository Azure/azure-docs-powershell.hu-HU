---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: a431428c670dba7e0bfb152bde0cae22f47d8099
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181182"
---
# <span data-ttu-id="10657-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="10657-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="10657-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10657-102">SYNOPSIS</span></span>
<span data-ttu-id="10657-103">Hozzáférést ad egy pillanatképhez.</span><span class="sxs-lookup"><span data-stu-id="10657-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="10657-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10657-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10657-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="10657-105">DESCRIPTION</span></span>
<span data-ttu-id="10657-106">A **Grant-AzSnapshotAccess** parancsmag hozzáférést ad egy pillanatképhez.</span><span class="sxs-lookup"><span data-stu-id="10657-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="10657-107">Példák</span><span class="sxs-lookup"><span data-stu-id="10657-107">EXAMPLES</span></span>

### <span data-ttu-id="10657-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="10657-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="10657-109">Adjon "READ" hozzáférést a "Snapshot01" nevű pillanatképhez a "ResourceGroup01" nevű erőforrás-csoportban, 60 másodperc múlva.</span><span class="sxs-lookup"><span data-stu-id="10657-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="10657-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10657-110">PARAMETERS</span></span>

### <span data-ttu-id="10657-111">-Access</span><span class="sxs-lookup"><span data-stu-id="10657-111">-Access</span></span>
<span data-ttu-id="10657-112">Hozzáférési szint megadása</span><span class="sxs-lookup"><span data-stu-id="10657-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10657-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10657-113">-AsJob</span></span>
<span data-ttu-id="10657-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="10657-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10657-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10657-115">-DefaultProfile</span></span>
<span data-ttu-id="10657-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10657-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10657-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="10657-117">-DurationInSecond</span></span>
<span data-ttu-id="10657-118">A hozzáférési időtartamot másodpercben adja meg.</span><span class="sxs-lookup"><span data-stu-id="10657-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10657-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10657-119">-ResourceGroupName</span></span>
<span data-ttu-id="10657-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10657-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10657-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="10657-121">-SnapshotName</span></span>
<span data-ttu-id="10657-122">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10657-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10657-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="10657-123">-Confirm</span></span>
<span data-ttu-id="10657-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="10657-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10657-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10657-125">-WhatIf</span></span>
<span data-ttu-id="10657-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="10657-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10657-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="10657-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10657-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10657-128">CommonParameters</span></span>
<span data-ttu-id="10657-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10657-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10657-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="10657-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10657-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10657-131">INPUTS</span></span>

### <span data-ttu-id="10657-132">System. String</span><span class="sxs-lookup"><span data-stu-id="10657-132">System.String</span></span>

## <span data-ttu-id="10657-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10657-133">OUTPUTS</span></span>

### <span data-ttu-id="10657-134">Microsoft. Azure. commands. számítási. Automation. models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="10657-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="10657-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10657-135">NOTES</span></span>

## <span data-ttu-id="10657-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10657-136">RELATED LINKS</span></span>
