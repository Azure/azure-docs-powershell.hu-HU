---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 35e767c340d5418ae500c4cc87a4b40741d8ba6a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204799"
---
# <span data-ttu-id="8a775-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="8a775-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="8a775-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a775-102">SYNOPSIS</span></span>
<span data-ttu-id="8a775-103">Egy pillanatfelvételhez való hozzáférés visszavonása.</span><span class="sxs-lookup"><span data-stu-id="8a775-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="8a775-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8a775-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a775-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8a775-105">DESCRIPTION</span></span>
<span data-ttu-id="8a775-106">A **Revoke-AzSnapshotAccess** parancsmag visszavonja a pillanatképhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="8a775-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="8a775-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8a775-107">EXAMPLES</span></span>

### <span data-ttu-id="8a775-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8a775-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="8a775-109">Az "Erőforráscsoport01" erőforráscsoport "Snapshot01" nevű pillanatképének hozzáférésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="8a775-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="8a775-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a775-110">PARAMETERS</span></span>

### <span data-ttu-id="8a775-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a775-111">-AsJob</span></span>
<span data-ttu-id="8a775-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8a775-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a775-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a775-113">-DefaultProfile</span></span>
<span data-ttu-id="8a775-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a775-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a775-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a775-115">-ResourceGroupName</span></span>
<span data-ttu-id="8a775-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a775-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8a775-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="8a775-117">-SnapshotName</span></span>
<span data-ttu-id="8a775-118">Egy pillanatfelvétel nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a775-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="8a775-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a775-119">-Confirm</span></span>
<span data-ttu-id="8a775-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8a775-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a775-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a775-121">-WhatIf</span></span>
<span data-ttu-id="8a775-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8a775-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a775-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8a775-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a775-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a775-124">CommonParameters</span></span>
<span data-ttu-id="8a775-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a775-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a775-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a775-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a775-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a775-127">INPUTS</span></span>

### <span data-ttu-id="8a775-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8a775-128">System.String</span></span>

## <span data-ttu-id="8a775-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a775-129">OUTPUTS</span></span>

### <span data-ttu-id="8a775-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8a775-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8a775-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8a775-131">NOTES</span></span>

## <span data-ttu-id="8a775-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a775-132">RELATED LINKS</span></span>
