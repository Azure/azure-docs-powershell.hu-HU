---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: ee5ae846ed83065b797f1389827d7d53ae1988d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015525"
---
# <span data-ttu-id="770fb-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="770fb-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="770fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770fb-102">SYNOPSIS</span></span>
<span data-ttu-id="770fb-103">A Batch-fiók kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="770fb-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="770fb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="770fb-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="770fb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="770fb-105">DESCRIPTION</span></span>
<span data-ttu-id="770fb-106">A **New-AzBatchAccountKey** parancsmag újragenerálja egy Azure Batch-fiók elsődleges vagy másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="770fb-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="770fb-107">A parancsmag egy **BatchAccountContext** objektumot ad vissza, amely az aktuális **PrimaryAccountKey és SecondaryAccountKey** tulajdonsággal rendelkezik. </span><span class="sxs-lookup"><span data-stu-id="770fb-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="770fb-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="770fb-108">EXAMPLES</span></span>

### <span data-ttu-id="770fb-109">1. példa: Az elsődleges fiókkulcs újragenerálása egy Batch-fiókban</span><span class="sxs-lookup"><span data-stu-id="770fb-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="770fb-110">Ez a parancs újra létrehozza az elsődleges fiókkulcsot a pfuller nevű Batch-fiókban.</span><span class="sxs-lookup"><span data-stu-id="770fb-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="770fb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="770fb-111">PARAMETERS</span></span>

### <span data-ttu-id="770fb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="770fb-112">-AccountName</span></span>
<span data-ttu-id="770fb-113">Annak a Batch-fióknak a nevét adja meg, amelynek a parancsmagja újragenerálja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="770fb-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770fb-114">-DefaultProfile</span></span>
<span data-ttu-id="770fb-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="770fb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="770fb-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="770fb-116">-KeyType</span></span>
<span data-ttu-id="770fb-117">A parancsmag által újragenerált kulcs típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="770fb-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="770fb-118">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="770fb-118">Valid values are:</span></span>
- <span data-ttu-id="770fb-119">Elsődleges</span><span class="sxs-lookup"><span data-stu-id="770fb-119">Primary</span></span>
- <span data-ttu-id="770fb-120">Másodlagos</span><span class="sxs-lookup"><span data-stu-id="770fb-120">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770fb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770fb-121">-ResourceGroupName</span></span>
<span data-ttu-id="770fb-122">Annak a fióknak az erőforráscsoportját adja meg, amelyhez ez a parancsmag újragenerálja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="770fb-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770fb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770fb-123">CommonParameters</span></span>
<span data-ttu-id="770fb-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770fb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770fb-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="770fb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770fb-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="770fb-126">INPUTS</span></span>

### <span data-ttu-id="770fb-127">System.String</span><span class="sxs-lookup"><span data-stu-id="770fb-127">System.String</span></span>

## <span data-ttu-id="770fb-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="770fb-128">OUTPUTS</span></span>

### <span data-ttu-id="770fb-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="770fb-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="770fb-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="770fb-130">NOTES</span></span>

## <span data-ttu-id="770fb-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="770fb-131">RELATED LINKS</span></span>

[<span data-ttu-id="770fb-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="770fb-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="770fb-133">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="770fb-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
