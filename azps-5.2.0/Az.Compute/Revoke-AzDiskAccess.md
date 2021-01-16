---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 76fb2e7483bb510d5eceb92b51f7e5e538c3b22b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344981"
---
# <span data-ttu-id="da91b-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="da91b-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="da91b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da91b-102">SYNOPSIS</span></span>
<span data-ttu-id="da91b-103">Lemezhez való hozzáférés visszavonása.</span><span class="sxs-lookup"><span data-stu-id="da91b-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="da91b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da91b-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da91b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da91b-105">DESCRIPTION</span></span>
<span data-ttu-id="da91b-106">A **Revoke-AzDiskAccess** parancsmag visszavonja a lemezhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="da91b-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="da91b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da91b-107">EXAMPLES</span></span>

### <span data-ttu-id="da91b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="da91b-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="da91b-109">A "Disk01" lemezhez való hozzáférés visszavonása az "ResourceGroup01" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="da91b-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="da91b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da91b-110">PARAMETERS</span></span>

### <span data-ttu-id="da91b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da91b-111">-AsJob</span></span>
<span data-ttu-id="da91b-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="da91b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da91b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da91b-113">-DefaultProfile</span></span>
<span data-ttu-id="da91b-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da91b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da91b-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="da91b-115">-DiskName</span></span>
<span data-ttu-id="da91b-116">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da91b-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="da91b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da91b-117">-ResourceGroupName</span></span>
<span data-ttu-id="da91b-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da91b-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="da91b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da91b-119">-Confirm</span></span>
<span data-ttu-id="da91b-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="da91b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da91b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da91b-121">-WhatIf</span></span>
<span data-ttu-id="da91b-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="da91b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da91b-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da91b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da91b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da91b-124">CommonParameters</span></span>
<span data-ttu-id="da91b-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da91b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da91b-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da91b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da91b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da91b-127">INPUTS</span></span>

### <span data-ttu-id="da91b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="da91b-128">System.String</span></span>

## <span data-ttu-id="da91b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da91b-129">OUTPUTS</span></span>

### <span data-ttu-id="da91b-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="da91b-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="da91b-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da91b-131">NOTES</span></span>

## <span data-ttu-id="da91b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da91b-132">RELATED LINKS</span></span>
