---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
ms.openlocfilehash: 7f1747d838d0b81d1cfa29e98134897357f33a53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493259"
---
# <span data-ttu-id="cc70c-101">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="cc70c-101">Set-AzureRmBatchAccount</span></span>

## <span data-ttu-id="cc70c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc70c-102">SYNOPSIS</span></span>
<span data-ttu-id="cc70c-103">Egy köteg-fiók frissítése</span><span class="sxs-lookup"><span data-stu-id="cc70c-103">Updates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc70c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc70c-104">SYNTAX</span></span>

```
Set-AzureRmBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc70c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc70c-105">DESCRIPTION</span></span>
<span data-ttu-id="cc70c-106">A **set-AzureRmBatchAccount** parancsmag egy Azure-köteg-fiókot frissít.</span><span class="sxs-lookup"><span data-stu-id="cc70c-106">The **Set-AzureRmBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="cc70c-107">Ez a parancsmag jelenleg csak címkéket tud frissíteni.</span><span class="sxs-lookup"><span data-stu-id="cc70c-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="cc70c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cc70c-108">EXAMPLES</span></span>

### <span data-ttu-id="cc70c-109">Példa 1: a címkék frissítése egy köteg fiókban</span><span class="sxs-lookup"><span data-stu-id="cc70c-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="cc70c-110">Ez a parancs frissíti a címkéket a pfuller nevű fiókban.</span><span class="sxs-lookup"><span data-stu-id="cc70c-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="cc70c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc70c-111">PARAMETERS</span></span>

### <span data-ttu-id="cc70c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cc70c-112">-AccountName</span></span>
<span data-ttu-id="cc70c-113">Annak a kötegelt fióknak a nevét adja meg, amelyre a parancsmag frissíti.</span><span class="sxs-lookup"><span data-stu-id="cc70c-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc70c-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cc70c-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="cc70c-115">Az automatikus tárterülethez használandó tárolási fiók erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc70c-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc70c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc70c-116">-DefaultProfile</span></span>
<span data-ttu-id="cc70c-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc70c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc70c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc70c-118">-ResourceGroupName</span></span>
<span data-ttu-id="cc70c-119">Annak a fióknak az erőforrás csoportját adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="cc70c-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc70c-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="cc70c-120">-Tag</span></span>
<span data-ttu-id="cc70c-121">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="cc70c-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cc70c-122">Példa:</span><span class="sxs-lookup"><span data-stu-id="cc70c-122">For example:</span></span>

<span data-ttu-id="cc70c-123">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="cc70c-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc70c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc70c-124">CommonParameters</span></span>
<span data-ttu-id="cc70c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc70c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc70c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc70c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc70c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc70c-127">INPUTS</span></span>

### <span data-ttu-id="cc70c-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="cc70c-128">None</span></span>
<span data-ttu-id="cc70c-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cc70c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cc70c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc70c-130">OUTPUTS</span></span>

### <span data-ttu-id="cc70c-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cc70c-131">BatchAccountContext</span></span>

## <span data-ttu-id="cc70c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc70c-132">NOTES</span></span>

## <span data-ttu-id="cc70c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc70c-133">RELATED LINKS</span></span>

[<span data-ttu-id="cc70c-134">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="cc70c-134">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="cc70c-135">Új – AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="cc70c-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="cc70c-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="cc70c-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="cc70c-137">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="cc70c-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
