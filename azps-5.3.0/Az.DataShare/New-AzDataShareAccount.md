---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: b24fe9e6587fe50a41d601c70c2687891bea2f16
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377255"
---
# <span data-ttu-id="9dae9-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="9dae9-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="9dae9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dae9-102">SYNOPSIS</span></span>
<span data-ttu-id="9dae9-103">Új adat-megosztási fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="9dae9-103">Creates new data share account</span></span>

## <span data-ttu-id="9dae9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9dae9-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dae9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9dae9-105">DESCRIPTION</span></span>
<span data-ttu-id="9dae9-106">**A New-AzDataShareAccount** parancsmag létrehoz egy adatmegosztási fiókot a megadott Azure-erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="9dae9-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="9dae9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9dae9-107">EXAMPLES</span></span>

### <span data-ttu-id="9dae9-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9dae9-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="9dae9-109">Létrehozza a "WikiADS" nevű fiókot az "ADS" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="9dae9-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="9dae9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dae9-110">PARAMETERS</span></span>

### <span data-ttu-id="9dae9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dae9-111">-AsJob</span></span>
<span data-ttu-id="9dae9-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="9dae9-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="9dae9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dae9-113">-DefaultProfile</span></span>
<span data-ttu-id="9dae9-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9dae9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dae9-115">-Location</span><span class="sxs-lookup"><span data-stu-id="9dae9-115">-Location</span></span>
<span data-ttu-id="9dae9-116">Az adat-megosztási fiók létrehozására használt hely.</span><span class="sxs-lookup"><span data-stu-id="9dae9-116">The location in which to create the data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dae9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9dae9-117">-Name</span></span>
<span data-ttu-id="9dae9-118">Azure data share account name.</span><span class="sxs-lookup"><span data-stu-id="9dae9-118">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dae9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dae9-119">-ResourceGroupName</span></span>
<span data-ttu-id="9dae9-120">A rendszer létrehoz egy erőforráscsoportot az Azure-adat-megosztási fiókban.</span><span class="sxs-lookup"><span data-stu-id="9dae9-120">The resource group name of the azure data share account will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dae9-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="9dae9-121">-Tag</span></span>
<span data-ttu-id="9dae9-122">Az Azure-adat-megosztási fiókkal társítani szükséges címkék.</span><span class="sxs-lookup"><span data-stu-id="9dae9-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dae9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dae9-123">-Confirm</span></span>
<span data-ttu-id="9dae9-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9dae9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dae9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dae9-125">-WhatIf</span></span>
<span data-ttu-id="9dae9-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9dae9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dae9-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9dae9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dae9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dae9-128">CommonParameters</span></span>
<span data-ttu-id="9dae9-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dae9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dae9-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dae9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dae9-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9dae9-131">INPUTS</span></span>

### <span data-ttu-id="9dae9-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="9dae9-132">None</span></span>

## <span data-ttu-id="9dae9-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dae9-133">OUTPUTS</span></span>

### <span data-ttu-id="9dae9-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="9dae9-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="9dae9-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9dae9-135">NOTES</span></span>

## <span data-ttu-id="9dae9-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dae9-136">RELATED LINKS</span></span>
