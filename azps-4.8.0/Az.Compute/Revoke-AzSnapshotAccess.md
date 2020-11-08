---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 35e767c340d5418ae500c4cc87a4b40741d8ba6a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025730"
---
# <span data-ttu-id="bb481-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="bb481-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="bb481-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb481-102">SYNOPSIS</span></span>
<span data-ttu-id="bb481-103">A pillanatképhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="bb481-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="bb481-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb481-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb481-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb481-105">DESCRIPTION</span></span>
<span data-ttu-id="bb481-106">A **Visszavonás-AzSnapshotAccess** parancsmag visszavonja a pillanatképhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="bb481-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="bb481-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bb481-107">EXAMPLES</span></span>

### <span data-ttu-id="bb481-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bb481-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="bb481-109">A "ResourceGroup01" nevű erőforráscsoport "Snapshot01" nevű pillanatképéhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="bb481-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="bb481-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb481-110">PARAMETERS</span></span>

### <span data-ttu-id="bb481-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb481-111">-AsJob</span></span>
<span data-ttu-id="bb481-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bb481-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb481-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb481-113">-DefaultProfile</span></span>
<span data-ttu-id="bb481-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb481-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb481-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb481-115">-ResourceGroupName</span></span>
<span data-ttu-id="bb481-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb481-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bb481-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="bb481-117">-SnapshotName</span></span>
<span data-ttu-id="bb481-118">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb481-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="bb481-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bb481-119">-Confirm</span></span>
<span data-ttu-id="bb481-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bb481-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb481-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb481-121">-WhatIf</span></span>
<span data-ttu-id="bb481-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bb481-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb481-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb481-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb481-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb481-124">CommonParameters</span></span>
<span data-ttu-id="bb481-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb481-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb481-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bb481-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb481-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb481-127">INPUTS</span></span>

### <span data-ttu-id="bb481-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bb481-128">System.String</span></span>

## <span data-ttu-id="bb481-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb481-129">OUTPUTS</span></span>

### <span data-ttu-id="bb481-130">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="bb481-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="bb481-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb481-131">NOTES</span></span>

## <span data-ttu-id="bb481-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb481-132">RELATED LINKS</span></span>
