---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: e996e02c9609e259c0833cfe179f295206684351
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93848010"
---
# <span data-ttu-id="796bd-101">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="796bd-101">New-AzBatchAccount</span></span>

## <span data-ttu-id="796bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="796bd-102">SYNOPSIS</span></span>
<span data-ttu-id="796bd-103">Köteg fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="796bd-103">Creates a Batch account.</span></span>

## <span data-ttu-id="796bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="796bd-104">SYNTAX</span></span>

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="796bd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="796bd-105">DESCRIPTION</span></span>
<span data-ttu-id="796bd-106">A **New-AzBatchAccount** parancsmag egy Azure-köteg típusú fiókot hoz létre a megadott erőforrás-csoporthoz és-helyhez.</span><span class="sxs-lookup"><span data-stu-id="796bd-106">The **New-AzBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="796bd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="796bd-107">EXAMPLES</span></span>

### <span data-ttu-id="796bd-108">1. példa: köteg fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="796bd-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="796bd-109">Ez a parancs a pfuller nevű köteg fiókot hoz létre a Nyugat-amerikai ResourceGroup03-erőforráscsoport használatával.</span><span class="sxs-lookup"><span data-stu-id="796bd-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="796bd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="796bd-110">PARAMETERS</span></span>

### <span data-ttu-id="796bd-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="796bd-111">-AccountName</span></span>
<span data-ttu-id="796bd-112">A parancsmag által létrehozott köteg fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="796bd-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="796bd-113">A köteg fiók nevének három és 24 karakter között kell lennie, és csak számokat és kisbetűket tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="796bd-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="796bd-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="796bd-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="796bd-115">Az automatikus tárterülethez használandó tárolási fiók erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="796bd-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="796bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="796bd-116">-DefaultProfile</span></span>
<span data-ttu-id="796bd-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="796bd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="796bd-118">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="796bd-118">-KeyVaultId</span></span>
<span data-ttu-id="796bd-119">A köteg fiókhoz társított Azure-kulcs erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="796bd-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="796bd-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="796bd-120">-KeyVaultUrl</span></span>
<span data-ttu-id="796bd-121">A köteg fiókhoz társított Azure Key Vault URL-címe.</span><span class="sxs-lookup"><span data-stu-id="796bd-121">The URL of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="796bd-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="796bd-122">-Location</span></span>
<span data-ttu-id="796bd-123">Azt a régiót adja meg, ahol ez a parancsmag hozza létre a fiókot.</span><span class="sxs-lookup"><span data-stu-id="796bd-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="796bd-124">További tudnivalókat az [Azure Regions](https://azure.microsoft.com/en-us/regions)című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="796bd-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="796bd-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="796bd-125">-PoolAllocationMode</span></span>
<span data-ttu-id="796bd-126">Gyűjtői mód a kötegek létrehozásához a köteg fiókban.</span><span class="sxs-lookup"><span data-stu-id="796bd-126">The allocation mode for creating pools in the Batch account.</span></span>

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

### <span data-ttu-id="796bd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="796bd-127">-ResourceGroupName</span></span>
<span data-ttu-id="796bd-128">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag létrehozza a fiókot.</span><span class="sxs-lookup"><span data-stu-id="796bd-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="796bd-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="796bd-129">-Tag</span></span>
<span data-ttu-id="796bd-130">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="796bd-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="796bd-131">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="796bd-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="796bd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="796bd-132">CommonParameters</span></span>
<span data-ttu-id="796bd-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="796bd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="796bd-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="796bd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="796bd-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="796bd-135">INPUTS</span></span>

### <span data-ttu-id="796bd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="796bd-136">System.String</span></span>

### <span data-ttu-id="796bd-137">System. null ' 1 [[Microsoft.Azure.Management.BatCH. Modellek. PoolAllocationMode, Microsoft.Azure.Management.BatCH, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="796bd-137">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="796bd-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="796bd-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="796bd-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="796bd-139">OUTPUTS</span></span>

### <span data-ttu-id="796bd-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="796bd-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="796bd-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="796bd-141">NOTES</span></span>

## <span data-ttu-id="796bd-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="796bd-142">RELATED LINKS</span></span>

[<span data-ttu-id="796bd-143">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="796bd-143">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="796bd-144">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="796bd-144">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="796bd-145">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="796bd-145">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="796bd-146">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="796bd-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
