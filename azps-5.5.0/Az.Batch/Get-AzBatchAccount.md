---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 66bab11ab5632464eed8ee160df527b0e44f053d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205351"
---
# <span data-ttu-id="59c8f-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="59c8f-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="59c8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="59c8f-103">Kötegfiókot kap az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="59c8f-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="59c8f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59c8f-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59c8f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59c8f-105">DESCRIPTION</span></span>
<span data-ttu-id="59c8f-106">A **Get-AzBatchAccount** parancsmag egy Azure Batch-fiókot kap az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="59c8f-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="59c8f-107">Az *AccountName* paramétert használva egyetlen fiókot kaphat, vagy az *ResourceGroupName* paramétert használva az adott erőforráscsoporthoz tartozik fiókokat is be tud szerezni.</span><span class="sxs-lookup"><span data-stu-id="59c8f-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="59c8f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59c8f-108">EXAMPLES</span></span>

### <span data-ttu-id="59c8f-109">1. példa: Batch-fiók lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="59c8f-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="59c8f-110">Ez a parancs a pfuller nevű kötegfiókot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59c8f-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="59c8f-111">2. példa: Erőforráscsoporthoz társított kötegfiókok lekérte</span><span class="sxs-lookup"><span data-stu-id="59c8f-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="59c8f-112">Ez a parancs a CmdletExampleRG erőforráscsoporthoz társított kötegfiókokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59c8f-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="59c8f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59c8f-113">PARAMETERS</span></span>

### <span data-ttu-id="59c8f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="59c8f-114">-AccountName</span></span>
<span data-ttu-id="59c8f-115">Egy fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59c8f-115">Specifies the name of an account.</span></span>
<span data-ttu-id="59c8f-116">Ha megad egy fióknevet, ez a parancsmag csak az adott fiókot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="59c8f-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59c8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c8f-117">-DefaultProfile</span></span>
<span data-ttu-id="59c8f-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59c8f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59c8f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c8f-119">-ResourceGroupName</span></span>
<span data-ttu-id="59c8f-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59c8f-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="59c8f-121">Ha megad egy erőforráscsoportot, ez a parancsmag a megadott erőforráscsoportba kapja a fiókokat.</span><span class="sxs-lookup"><span data-stu-id="59c8f-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59c8f-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="59c8f-122">-Tag</span></span>
<span data-ttu-id="59c8f-123">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="59c8f-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="59c8f-124">Például: @{key0="érték0";key1=$null;key2="érték2"} Ez a parancsmag olyan fiókokat kap, amelyek a paraméter által megadott címkéket tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="59c8f-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59c8f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c8f-125">CommonParameters</span></span>
<span data-ttu-id="59c8f-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c8f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c8f-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59c8f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c8f-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59c8f-128">INPUTS</span></span>

### <span data-ttu-id="59c8f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="59c8f-129">System.String</span></span>

### <span data-ttu-id="59c8f-130">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="59c8f-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="59c8f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59c8f-131">OUTPUTS</span></span>

### <span data-ttu-id="59c8f-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="59c8f-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="59c8f-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59c8f-133">NOTES</span></span>

## <span data-ttu-id="59c8f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59c8f-134">RELATED LINKS</span></span>

[<span data-ttu-id="59c8f-135">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="59c8f-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="59c8f-136">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="59c8f-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="59c8f-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="59c8f-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="59c8f-138">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c8f-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
