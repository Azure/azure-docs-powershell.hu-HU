---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933058"
---
# <span data-ttu-id="2a7ca-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2a7ca-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="2a7ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="2a7ca-103">Lemezelérési erőforrást hoz létre</span><span class="sxs-lookup"><span data-stu-id="2a7ca-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="2a7ca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2a7ca-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a7ca-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2a7ca-105">DESCRIPTION</span></span>
<span data-ttu-id="2a7ca-106">A **New-AzDiskAccess** parancsmag lemezelérési erőforrást hoz létre</span><span class="sxs-lookup"><span data-stu-id="2a7ca-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="2a7ca-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2a7ca-107">EXAMPLES</span></span>

### <span data-ttu-id="2a7ca-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2a7ca-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="2a7ca-109">Ezzel a paranccsal lemezelérést hozhat létre adott tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="2a7ca-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="2a7ca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a7ca-110">PARAMETERS</span></span>

### <span data-ttu-id="2a7ca-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a7ca-111">-AsJob</span></span>
<span data-ttu-id="2a7ca-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2a7ca-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a7ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a7ca-113">-DefaultProfile</span></span>
<span data-ttu-id="2a7ca-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a7ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a7ca-115">-Location</span><span class="sxs-lookup"><span data-stu-id="2a7ca-115">-Location</span></span>
<span data-ttu-id="2a7ca-116">Megadja a helyet.</span><span class="sxs-lookup"><span data-stu-id="2a7ca-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7ca-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2a7ca-117">-Name</span></span>
<span data-ttu-id="2a7ca-118">A lemezelérés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a7ca-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7ca-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a7ca-119">-ResourceGroupName</span></span>
<span data-ttu-id="2a7ca-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a7ca-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2a7ca-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a7ca-121">-Confirm</span></span>
<span data-ttu-id="2a7ca-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2a7ca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a7ca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a7ca-123">-WhatIf</span></span>
<span data-ttu-id="2a7ca-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2a7ca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a7ca-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a7ca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a7ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a7ca-126">CommonParameters</span></span>
<span data-ttu-id="2a7ca-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a7ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a7ca-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a7ca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a7ca-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a7ca-129">INPUTS</span></span>

### <span data-ttu-id="2a7ca-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2a7ca-130">System.String</span></span>

## <span data-ttu-id="2a7ca-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a7ca-131">OUTPUTS</span></span>

### <span data-ttu-id="2a7ca-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2a7ca-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="2a7ca-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2a7ca-133">NOTES</span></span>

## <span data-ttu-id="2a7ca-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a7ca-134">RELATED LINKS</span></span>
