---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: 44627bd5ffa7340a10866605598d981b10f35a58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194819"
---
# <span data-ttu-id="62c1c-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="62c1c-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="62c1c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="62c1c-103">Egy köteg-fiók frissítése</span><span class="sxs-lookup"><span data-stu-id="62c1c-103">Updates a Batch account.</span></span>

## <span data-ttu-id="62c1c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62c1c-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62c1c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="62c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="62c1c-106">A **set-AzBatchAccount** parancsmag egy Azure-köteg-fiókot frissít.</span><span class="sxs-lookup"><span data-stu-id="62c1c-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="62c1c-107">Ez a parancsmag jelenleg csak címkéket tud frissíteni.</span><span class="sxs-lookup"><span data-stu-id="62c1c-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="62c1c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="62c1c-108">EXAMPLES</span></span>

### <span data-ttu-id="62c1c-109">Példa 1: a címkék frissítése egy köteg fiókban</span><span class="sxs-lookup"><span data-stu-id="62c1c-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
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

<span data-ttu-id="62c1c-110">Ez a parancs frissíti a címkéket a pfuller nevű fiókban.</span><span class="sxs-lookup"><span data-stu-id="62c1c-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="62c1c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62c1c-111">PARAMETERS</span></span>

### <span data-ttu-id="62c1c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="62c1c-112">-AccountName</span></span>
<span data-ttu-id="62c1c-113">Annak a kötegelt fióknak a nevét adja meg, amelyre a parancsmag frissíti.</span><span class="sxs-lookup"><span data-stu-id="62c1c-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="62c1c-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="62c1c-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="62c1c-115">Az automatikus tárterülethez használandó tárolási fiók erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="62c1c-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="62c1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c1c-116">-DefaultProfile</span></span>
<span data-ttu-id="62c1c-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62c1c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62c1c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c1c-118">-ResourceGroupName</span></span>
<span data-ttu-id="62c1c-119">Annak a fióknak az erőforrás csoportját adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="62c1c-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="62c1c-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="62c1c-120">-Tag</span></span>
<span data-ttu-id="62c1c-121">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="62c1c-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="62c1c-122">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="62c1c-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c1c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c1c-123">CommonParameters</span></span>
<span data-ttu-id="62c1c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62c1c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c1c-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="62c1c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c1c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62c1c-126">INPUTS</span></span>

### <span data-ttu-id="62c1c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="62c1c-127">System.String</span></span>

### <span data-ttu-id="62c1c-128">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="62c1c-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="62c1c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62c1c-129">OUTPUTS</span></span>

### <span data-ttu-id="62c1c-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="62c1c-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="62c1c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62c1c-131">NOTES</span></span>

## <span data-ttu-id="62c1c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62c1c-132">RELATED LINKS</span></span>

[<span data-ttu-id="62c1c-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="62c1c-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="62c1c-134">Új – AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="62c1c-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="62c1c-135">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="62c1c-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="62c1c-136">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="62c1c-136">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
