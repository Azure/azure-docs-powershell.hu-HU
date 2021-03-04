---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: b18db3b4e8448212b413dc13887ea68b35f22422
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919010"
---
# <span data-ttu-id="63bad-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="63bad-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="63bad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63bad-102">SYNOPSIS</span></span>
<span data-ttu-id="63bad-103">Egy pillanatfelvételhez való hozzáférés visszavonása.</span><span class="sxs-lookup"><span data-stu-id="63bad-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="63bad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="63bad-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63bad-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="63bad-105">DESCRIPTION</span></span>
<span data-ttu-id="63bad-106">A **Revoke-AzSnapshotAccess** parancsmag visszavonja a pillanatképhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="63bad-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="63bad-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="63bad-107">EXAMPLES</span></span>

### <span data-ttu-id="63bad-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="63bad-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="63bad-109">Az "Erőforráscsoport01" erőforráscsoport "Snapshot01" nevű pillanatképének hozzáférésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="63bad-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="63bad-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63bad-110">PARAMETERS</span></span>

### <span data-ttu-id="63bad-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63bad-111">-AsJob</span></span>
<span data-ttu-id="63bad-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="63bad-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63bad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63bad-113">-DefaultProfile</span></span>
<span data-ttu-id="63bad-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63bad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63bad-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63bad-115">-ResourceGroupName</span></span>
<span data-ttu-id="63bad-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="63bad-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="63bad-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="63bad-117">-SnapshotName</span></span>
<span data-ttu-id="63bad-118">Egy pillanatfelvétel nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="63bad-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="63bad-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63bad-119">-Confirm</span></span>
<span data-ttu-id="63bad-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="63bad-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63bad-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63bad-121">-WhatIf</span></span>
<span data-ttu-id="63bad-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="63bad-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63bad-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63bad-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63bad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63bad-124">CommonParameters</span></span>
<span data-ttu-id="63bad-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63bad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63bad-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63bad-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63bad-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63bad-127">INPUTS</span></span>

### <span data-ttu-id="63bad-128">System.String</span><span class="sxs-lookup"><span data-stu-id="63bad-128">System.String</span></span>

## <span data-ttu-id="63bad-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63bad-129">OUTPUTS</span></span>

### <span data-ttu-id="63bad-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="63bad-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="63bad-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="63bad-131">NOTES</span></span>

## <span data-ttu-id="63bad-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63bad-132">RELATED LINKS</span></span>
