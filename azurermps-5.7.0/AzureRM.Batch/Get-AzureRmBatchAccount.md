---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: 7fd0283860fd5a0bbca1376afff00c8d4add29b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493260"
---
# <span data-ttu-id="56207-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="56207-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="56207-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56207-102">SYNOPSIS</span></span>
<span data-ttu-id="56207-103">A jelenlegi előfizetésből kapja meg a köteg-fiókot.</span><span class="sxs-lookup"><span data-stu-id="56207-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56207-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56207-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56207-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="56207-105">DESCRIPTION</span></span>
<span data-ttu-id="56207-106">A **Get-AzureRmBatchAccount** parancsmag Azure-köteg-fiókot kap az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="56207-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="56207-107">A *accountname* paraméterrel egyetlen fiókot kaphat, vagy a *ResourceGroupName* paraméterrel lekérheti az adott erőforráscsoport fiókját.</span><span class="sxs-lookup"><span data-stu-id="56207-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="56207-108">Példák</span><span class="sxs-lookup"><span data-stu-id="56207-108">EXAMPLES</span></span>

### <span data-ttu-id="56207-109">Példa 1: köteg-fiók beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="56207-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzureRmBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="56207-110">Ez a parancs a pfuller nevű köteg fiókot kapja.</span><span class="sxs-lookup"><span data-stu-id="56207-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="56207-111">2. példa: az erőforráscsoport által társított köteg-számlák beolvasása</span><span class="sxs-lookup"><span data-stu-id="56207-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzureRmBatchAccount -ResourceGroupName "CmdletExampleRG"
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

<span data-ttu-id="56207-112">Ez a parancs beolvassa a CmdletExampleRG-erőforráscsoport társított köteg-fiókjait.</span><span class="sxs-lookup"><span data-stu-id="56207-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="56207-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56207-113">PARAMETERS</span></span>

### <span data-ttu-id="56207-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="56207-114">-AccountName</span></span>
<span data-ttu-id="56207-115">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="56207-115">Specifies the name of an account.</span></span>
<span data-ttu-id="56207-116">Ha megad egy fióknevet, ez a parancsmag csak azt a fiókot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="56207-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56207-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56207-117">-DefaultProfile</span></span>
<span data-ttu-id="56207-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56207-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56207-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56207-119">-ResourceGroupName</span></span>
<span data-ttu-id="56207-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="56207-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="56207-121">Ha egy erőforráscsoport beállítását adja meg, ez a parancsmag a megadott erőforráscsoport alatti fiókokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="56207-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56207-122">-Címke</span><span class="sxs-lookup"><span data-stu-id="56207-122">-Tag</span></span>
<span data-ttu-id="56207-123">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="56207-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="56207-124">Példa:</span><span class="sxs-lookup"><span data-stu-id="56207-124">For example:</span></span>

<span data-ttu-id="56207-125">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="56207-125">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="56207-126">Ez a parancsmag olyan fiókokat kap, amelyek a paraméter által megadott címkéket tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="56207-126">This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56207-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56207-127">CommonParameters</span></span>
<span data-ttu-id="56207-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56207-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56207-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56207-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56207-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56207-130">INPUTS</span></span>

### <span data-ttu-id="56207-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="56207-131">None</span></span>
<span data-ttu-id="56207-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="56207-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56207-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56207-133">OUTPUTS</span></span>

### <span data-ttu-id="56207-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="56207-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="56207-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56207-135">NOTES</span></span>

## <span data-ttu-id="56207-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56207-136">RELATED LINKS</span></span>

[<span data-ttu-id="56207-137">Új – AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="56207-137">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="56207-138">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="56207-138">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="56207-139">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="56207-139">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="56207-140">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="56207-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
