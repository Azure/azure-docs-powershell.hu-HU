---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 4e9a427a6e78848858773a1c661b949f91f0ffff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667313"
---
# <span data-ttu-id="245f5-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="245f5-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="245f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="245f5-102">SYNOPSIS</span></span>
<span data-ttu-id="245f5-103">Pillanatkép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="245f5-103">Removes a snapshot.</span></span>

## <span data-ttu-id="245f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="245f5-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="245f5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="245f5-105">DESCRIPTION</span></span>
<span data-ttu-id="245f5-106">A **Remove-AzSnapshot** parancsmag eltávolítja a pillanatképet.</span><span class="sxs-lookup"><span data-stu-id="245f5-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="245f5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="245f5-107">EXAMPLES</span></span>

### <span data-ttu-id="245f5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="245f5-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="245f5-109">Ez a parancs eltávolítja a "Snapshot01" nevű pillanatképet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="245f5-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="245f5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="245f5-110">PARAMETERS</span></span>

### <span data-ttu-id="245f5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="245f5-111">-AsJob</span></span>
<span data-ttu-id="245f5-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="245f5-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="245f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="245f5-113">-DefaultProfile</span></span>
<span data-ttu-id="245f5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="245f5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="245f5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="245f5-115">-Force</span></span>
<span data-ttu-id="245f5-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="245f5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="245f5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="245f5-117">-ResourceGroupName</span></span>
<span data-ttu-id="245f5-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="245f5-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="245f5-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="245f5-119">-SnapshotName</span></span>
<span data-ttu-id="245f5-120">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="245f5-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="245f5-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="245f5-121">-Confirm</span></span>
<span data-ttu-id="245f5-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="245f5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="245f5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="245f5-123">-WhatIf</span></span>
<span data-ttu-id="245f5-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="245f5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="245f5-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="245f5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="245f5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="245f5-126">CommonParameters</span></span>
<span data-ttu-id="245f5-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="245f5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="245f5-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="245f5-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="245f5-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="245f5-129">INPUTS</span></span>

### <span data-ttu-id="245f5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="245f5-130">System.String</span></span>

## <span data-ttu-id="245f5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="245f5-131">OUTPUTS</span></span>

### <span data-ttu-id="245f5-132">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="245f5-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="245f5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="245f5-133">NOTES</span></span>

## <span data-ttu-id="245f5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="245f5-134">RELATED LINKS</span></span>
