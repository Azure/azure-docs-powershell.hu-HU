---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: d634ab23912c45a0916ccf64244dda24190c6ee3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494163"
---
# <span data-ttu-id="301e1-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="301e1-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="301e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="301e1-102">SYNOPSIS</span></span>
<span data-ttu-id="301e1-103">Köteg fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="301e1-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="301e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="301e1-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="301e1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="301e1-105">DESCRIPTION</span></span>
<span data-ttu-id="301e1-106">A **New-AzureRmBatchAccount** parancsmag egy Azure-köteg típusú fiókot hoz létre a megadott erőforrás-csoporthoz és-helyhez.</span><span class="sxs-lookup"><span data-stu-id="301e1-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="301e1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="301e1-107">EXAMPLES</span></span>

### <span data-ttu-id="301e1-108">1. példa: köteg fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="301e1-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="301e1-109">Ez a parancs a pfuller nevű köteg fiókot hoz létre a Nyugat-amerikai ResourceGroup03-erőforráscsoport használatával.</span><span class="sxs-lookup"><span data-stu-id="301e1-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="301e1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="301e1-110">PARAMETERS</span></span>

### <span data-ttu-id="301e1-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="301e1-111">-AccountName</span></span>
<span data-ttu-id="301e1-112">A parancsmag által létrehozott köteg fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="301e1-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="301e1-113">A köteg fiók nevének három és 24 karakter között kell lennie, és csak számokat és kisbetűket tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="301e1-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="301e1-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="301e1-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="301e1-115">Az automatikus tárterülethez használandó tárolási fiók erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="301e1-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301e1-116">-DefaultProfile</span></span>
<span data-ttu-id="301e1-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="301e1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301e1-118">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="301e1-118">-KeyVaultId</span></span>
<span data-ttu-id="301e1-119">A köteg fiókhoz társított Azure-kulcs erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="301e1-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="301e1-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="301e1-120">-KeyVaultUrl</span></span>
<span data-ttu-id="301e1-121">A köteg fiókhoz társított Azure Key Vault URL-címe.</span><span class="sxs-lookup"><span data-stu-id="301e1-121">The URL of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="301e1-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="301e1-122">-Location</span></span>
<span data-ttu-id="301e1-123">Azt a régiót adja meg, ahol ez a parancsmag hozza létre a fiókot.</span><span class="sxs-lookup"><span data-stu-id="301e1-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="301e1-124">További tudnivalókat az [Azure Regions](https://azure.microsoft.com/en-us/regions)című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="301e1-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301e1-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="301e1-125">-PoolAllocationMode</span></span>
<span data-ttu-id="301e1-126">Gyűjtői mód a kötegek létrehozásához a köteg fiókban.</span><span class="sxs-lookup"><span data-stu-id="301e1-126">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode]
Parameter Sets: (All)
Aliases:
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301e1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301e1-127">-ResourceGroupName</span></span>
<span data-ttu-id="301e1-128">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag létrehozza a fiókot.</span><span class="sxs-lookup"><span data-stu-id="301e1-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301e1-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="301e1-129">-Tag</span></span>
<span data-ttu-id="301e1-130">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="301e1-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="301e1-131">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="301e1-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301e1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301e1-132">CommonParameters</span></span>
<span data-ttu-id="301e1-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="301e1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301e1-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="301e1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301e1-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="301e1-135">INPUTS</span></span>

### <span data-ttu-id="301e1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="301e1-136">System.String</span></span>

### <span data-ttu-id="301e1-137">System. null ' 1 [[Microsoft.Azure.Management.BatCH. Modellek. PoolAllocationMode, Microsoft.Azure.Management.BatCH, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="301e1-137">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="301e1-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="301e1-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="301e1-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="301e1-139">OUTPUTS</span></span>

### <span data-ttu-id="301e1-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="301e1-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="301e1-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="301e1-141">NOTES</span></span>

## <span data-ttu-id="301e1-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="301e1-142">RELATED LINKS</span></span>

[<span data-ttu-id="301e1-143">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="301e1-143">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="301e1-144">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="301e1-144">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="301e1-145">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="301e1-145">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="301e1-146">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="301e1-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
