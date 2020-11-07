---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 48080fde4c7187bcbcf601cb136373cc16ef7503
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847862"
---
# <span data-ttu-id="75d8f-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="75d8f-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="75d8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="75d8f-103">A jelenlegi előfizetésből kapja meg a köteg-fiókot.</span><span class="sxs-lookup"><span data-stu-id="75d8f-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="75d8f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75d8f-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75d8f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="75d8f-105">DESCRIPTION</span></span>
<span data-ttu-id="75d8f-106">A **Get-AzBatchAccount** parancsmag Azure-köteg-fiókot kap az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="75d8f-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="75d8f-107">A *accountname* paraméterrel egyetlen fiókot kaphat, vagy a *ResourceGroupName* paraméterrel lekérheti az adott erőforráscsoport fiókját.</span><span class="sxs-lookup"><span data-stu-id="75d8f-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="75d8f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="75d8f-108">EXAMPLES</span></span>

### <span data-ttu-id="75d8f-109">Példa 1: köteg-fiók beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="75d8f-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="75d8f-110">Ez a parancs a pfuller nevű köteg fiókot kapja.</span><span class="sxs-lookup"><span data-stu-id="75d8f-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="75d8f-111">2. példa: az erőforráscsoport által társított köteg-számlák beolvasása</span><span class="sxs-lookup"><span data-stu-id="75d8f-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="75d8f-112">Ez a parancs beolvassa a CmdletExampleRG-erőforráscsoport társított köteg-fiókjait.</span><span class="sxs-lookup"><span data-stu-id="75d8f-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="75d8f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75d8f-113">PARAMETERS</span></span>

### <span data-ttu-id="75d8f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75d8f-114">-AccountName</span></span>
<span data-ttu-id="75d8f-115">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75d8f-115">Specifies the name of an account.</span></span>
<span data-ttu-id="75d8f-116">Ha megad egy fióknevet, ez a parancsmag csak azt a fiókot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="75d8f-116">If you specify an account name, this cmdlet only returns that account.</span></span>

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

### <span data-ttu-id="75d8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d8f-117">-DefaultProfile</span></span>
<span data-ttu-id="75d8f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75d8f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75d8f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d8f-119">-ResourceGroupName</span></span>
<span data-ttu-id="75d8f-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75d8f-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="75d8f-121">Ha egy erőforráscsoport beállítását adja meg, ez a parancsmag a megadott erőforráscsoport alatti fiókokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="75d8f-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

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

### <span data-ttu-id="75d8f-122">-Címke</span><span class="sxs-lookup"><span data-stu-id="75d8f-122">-Tag</span></span>
<span data-ttu-id="75d8f-123">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="75d8f-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="75d8f-124">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"} Ez a parancsmag olyan fiókokat kap, amelyek a paraméter által megadott címkéket tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="75d8f-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

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

### <span data-ttu-id="75d8f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d8f-125">CommonParameters</span></span>
<span data-ttu-id="75d8f-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75d8f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d8f-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75d8f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d8f-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75d8f-128">INPUTS</span></span>

### <span data-ttu-id="75d8f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="75d8f-129">System.String</span></span>

### <span data-ttu-id="75d8f-130">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="75d8f-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="75d8f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75d8f-131">OUTPUTS</span></span>

### <span data-ttu-id="75d8f-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="75d8f-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="75d8f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75d8f-133">NOTES</span></span>

## <span data-ttu-id="75d8f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75d8f-134">RELATED LINKS</span></span>

[<span data-ttu-id="75d8f-135">Új – AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="75d8f-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="75d8f-136">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="75d8f-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="75d8f-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="75d8f-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="75d8f-138">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="75d8f-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)