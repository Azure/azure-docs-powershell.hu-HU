---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: 121e4b4b2ffe25d9e5ae53cb03e60cb7a1da91b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205215"
---
# <span data-ttu-id="bcbec-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="bcbec-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="bcbec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcbec-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbec-103">A Batch-fiók kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="bcbec-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="bcbec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bcbec-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcbec-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bcbec-105">DESCRIPTION</span></span>
<span data-ttu-id="bcbec-106">A **New-AzBatchAccountKey** parancsmag újragenerálja egy Azure Batch-fiók elsődleges vagy másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="bcbec-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="bcbec-107">A parancsmag egy **BatchAccountContext** objektumot ad vissza, amely az aktuális **PrimaryAccountKey** és **SecondaryAccountKey** tulajdonsággal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="bcbec-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="bcbec-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bcbec-108">EXAMPLES</span></span>

### <span data-ttu-id="bcbec-109">1. példa: Az elsődleges fiókkulcs újragenerálása egy Batch-fiókban</span><span class="sxs-lookup"><span data-stu-id="bcbec-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
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

<span data-ttu-id="bcbec-110">Ez a parancs újra létrehozza az elsődleges fiókkulcsot a pfuller nevű Batch-fiókban.</span><span class="sxs-lookup"><span data-stu-id="bcbec-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="bcbec-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcbec-111">PARAMETERS</span></span>

### <span data-ttu-id="bcbec-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bcbec-112">-AccountName</span></span>
<span data-ttu-id="bcbec-113">Annak a Batch-fióknak a nevét adja meg, amelynek a parancsmagja újragenerálja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="bcbec-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="bcbec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbec-114">-DefaultProfile</span></span>
<span data-ttu-id="bcbec-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bcbec-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcbec-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="bcbec-116">-KeyType</span></span>
<span data-ttu-id="bcbec-117">A parancsmag által újragenerált kulcs típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcbec-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="bcbec-118">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="bcbec-118">Valid values are:</span></span>
- <span data-ttu-id="bcbec-119">Elsődleges</span><span class="sxs-lookup"><span data-stu-id="bcbec-119">Primary</span></span>
- <span data-ttu-id="bcbec-120">Másodlagos</span><span class="sxs-lookup"><span data-stu-id="bcbec-120">Secondary</span></span>

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

### <span data-ttu-id="bcbec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcbec-121">-ResourceGroupName</span></span>
<span data-ttu-id="bcbec-122">Annak a fióknak az erőforráscsoportját adja meg, amelyhez ez a parancsmag újragenerálja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="bcbec-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="bcbec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbec-123">CommonParameters</span></span>
<span data-ttu-id="bcbec-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcbec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbec-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcbec-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbec-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcbec-126">INPUTS</span></span>

### <span data-ttu-id="bcbec-127">System.String</span><span class="sxs-lookup"><span data-stu-id="bcbec-127">System.String</span></span>

## <span data-ttu-id="bcbec-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcbec-128">OUTPUTS</span></span>

### <span data-ttu-id="bcbec-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bcbec-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bcbec-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bcbec-130">NOTES</span></span>

## <span data-ttu-id="bcbec-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcbec-131">RELATED LINKS</span></span>

[<span data-ttu-id="bcbec-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="bcbec-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bcbec-133">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bcbec-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
