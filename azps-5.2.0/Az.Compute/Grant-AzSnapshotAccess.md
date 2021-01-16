---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: a431428c670dba7e0bfb152bde0cae22f47d8099
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334314"
---
# <span data-ttu-id="7a6a4-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="7a6a4-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="7a6a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a6a4-102">SYNOPSIS</span></span>
<span data-ttu-id="7a6a4-103">Hozzáférést ad egy pillanatfelvételhez.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="7a6a4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7a6a4-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a6a4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7a6a4-105">DESCRIPTION</span></span>
<span data-ttu-id="7a6a4-106">A **Grant-AzSnapshotAccess** parancsmag hozzáférést biztosít egy pillanatfelvételhez.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="7a6a4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7a6a4-107">EXAMPLES</span></span>

### <span data-ttu-id="7a6a4-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7a6a4-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="7a6a4-109">60 másodpercig adjon olvasási hozzáférést az "Erőforráscsoport01" erőforráscsoport "Snapshot01" nevű pillanatképének.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="7a6a4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a6a4-110">PARAMETERS</span></span>

### <span data-ttu-id="7a6a4-111">-Access</span><span class="sxs-lookup"><span data-stu-id="7a6a4-111">-Access</span></span>
<span data-ttu-id="7a6a4-112">Az Access szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="7a6a4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a6a4-113">-AsJob</span></span>
<span data-ttu-id="7a6a4-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7a6a4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a6a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a6a4-115">-DefaultProfile</span></span>
<span data-ttu-id="7a6a4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a6a4-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="7a6a4-117">-DurationInSecond</span></span>
<span data-ttu-id="7a6a4-118">A hozzáférési időtartamot adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="7a6a4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a6a4-119">-ResourceGroupName</span></span>
<span data-ttu-id="7a6a4-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7a6a4-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="7a6a4-121">-SnapshotName</span></span>
<span data-ttu-id="7a6a4-122">Egy pillanatfelvétel nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="7a6a4-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a6a4-123">-Confirm</span></span>
<span data-ttu-id="7a6a4-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a6a4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a6a4-125">-WhatIf</span></span>
<span data-ttu-id="7a6a4-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a6a4-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a6a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a6a4-128">CommonParameters</span></span>
<span data-ttu-id="7a6a4-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a6a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a6a4-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a6a4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a6a4-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a6a4-131">INPUTS</span></span>

### <span data-ttu-id="7a6a4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7a6a4-132">System.String</span></span>

## <span data-ttu-id="7a6a4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a6a4-133">OUTPUTS</span></span>

### <span data-ttu-id="7a6a4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="7a6a4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="7a6a4-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7a6a4-135">NOTES</span></span>

## <span data-ttu-id="7a6a4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a6a4-136">RELATED LINKS</span></span>
