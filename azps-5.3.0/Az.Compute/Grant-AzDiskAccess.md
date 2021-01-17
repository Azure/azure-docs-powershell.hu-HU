---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 39565aa0675a0afc5f6f3996cad522b435a1a9b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480843"
---
# <span data-ttu-id="31b12-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="31b12-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="31b12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b12-102">SYNOPSIS</span></span>
<span data-ttu-id="31b12-103">Hozzáférést biztosít a lemezhez.</span><span class="sxs-lookup"><span data-stu-id="31b12-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="31b12-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="31b12-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31b12-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="31b12-105">DESCRIPTION</span></span>
<span data-ttu-id="31b12-106">A **Grant-AzDiskAccess** parancsmag hozzáférést biztosít a lemezhez.</span><span class="sxs-lookup"><span data-stu-id="31b12-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="31b12-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="31b12-107">EXAMPLES</span></span>

### <span data-ttu-id="31b12-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="31b12-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="31b12-109">Adjon olvasási hozzáférést a "Disk01" lemezhez az "ResourceGroup01" erőforráscsoportban 60 másodpercig.</span><span class="sxs-lookup"><span data-stu-id="31b12-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="31b12-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31b12-110">PARAMETERS</span></span>

### <span data-ttu-id="31b12-111">-Access</span><span class="sxs-lookup"><span data-stu-id="31b12-111">-Access</span></span>
<span data-ttu-id="31b12-112">Az Access szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31b12-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="31b12-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31b12-113">-AsJob</span></span>
<span data-ttu-id="31b12-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="31b12-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31b12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b12-115">-DefaultProfile</span></span>
<span data-ttu-id="31b12-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31b12-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b12-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="31b12-117">-DiskName</span></span>
<span data-ttu-id="31b12-118">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31b12-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="31b12-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="31b12-119">-DurationInSecond</span></span>
<span data-ttu-id="31b12-120">A hozzáférési időtartamot adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="31b12-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="31b12-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b12-121">-ResourceGroupName</span></span>
<span data-ttu-id="31b12-122">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31b12-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="31b12-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31b12-123">-Confirm</span></span>
<span data-ttu-id="31b12-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="31b12-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31b12-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b12-125">-WhatIf</span></span>
<span data-ttu-id="31b12-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="31b12-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31b12-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="31b12-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b12-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b12-128">CommonParameters</span></span>
<span data-ttu-id="31b12-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b12-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b12-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31b12-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b12-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31b12-131">INPUTS</span></span>

### <span data-ttu-id="31b12-132">System.String</span><span class="sxs-lookup"><span data-stu-id="31b12-132">System.String</span></span>

## <span data-ttu-id="31b12-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31b12-133">OUTPUTS</span></span>

### <span data-ttu-id="31b12-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="31b12-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="31b12-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="31b12-135">NOTES</span></span>

## <span data-ttu-id="31b12-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31b12-136">RELATED LINKS</span></span>
