---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: db35d5f6f0a8c8345fb10d13e4d2ca5c6169a090
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180623"
---
# <span data-ttu-id="b2505-101">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b2505-101">New-AzBatchAccount</span></span>

## <span data-ttu-id="b2505-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2505-102">SYNOPSIS</span></span>
<span data-ttu-id="b2505-103">Köteg fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b2505-103">Creates a Batch account.</span></span>

## <span data-ttu-id="b2505-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2505-104">SYNTAX</span></span>

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-PublicNetworkAccess <PublicNetworkAccessType>]
 [-IdentityType <ResourceIdentityType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2505-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2505-105">DESCRIPTION</span></span>
<span data-ttu-id="b2505-106">A **New-AzBatchAccount** parancsmag egy Azure-köteg típusú fiókot hoz létre a megadott erőforrás-csoporthoz és-helyhez.</span><span class="sxs-lookup"><span data-stu-id="b2505-106">The **New-AzBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="b2505-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b2505-107">EXAMPLES</span></span>

### <span data-ttu-id="b2505-108">1. példa: köteg fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="b2505-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="b2505-109">Ez a parancs a pfuller nevű köteg fiókot hoz létre a Nyugat-amerikai ResourceGroup03-erőforráscsoport használatával.</span><span class="sxs-lookup"><span data-stu-id="b2505-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="b2505-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2505-110">PARAMETERS</span></span>

### <span data-ttu-id="b2505-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b2505-111">-AccountName</span></span>
<span data-ttu-id="b2505-112">A parancsmag által létrehozott köteg fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2505-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="b2505-113">A köteg fiók nevének három és 24 karakter között kell lennie, és csak számokat és kisbetűket tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="b2505-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="b2505-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b2505-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="b2505-115">Az automatikus tárterülethez használandó tárolási fiók erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2505-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="b2505-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2505-116">-DefaultProfile</span></span>
<span data-ttu-id="b2505-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2505-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2505-118">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b2505-118">-IdentityType</span></span>
<span data-ttu-id="b2505-119">A BatchAccount társított identitás</span><span class="sxs-lookup"><span data-stu-id="b2505-119">The identity associated with the BatchAccount</span></span>

```yaml
Type: Microsoft.Azure.Management.Batch.Models.ResourceIdentityType
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2505-120">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="b2505-120">-KeyVaultId</span></span>
<span data-ttu-id="b2505-121">A köteg fiókhoz társított Azure-kulcs erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b2505-121">The resource ID of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="b2505-122">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="b2505-122">-KeyVaultUrl</span></span>
<span data-ttu-id="b2505-123">A köteg fiókhoz társított Azure Key Vault URL-címe.</span><span class="sxs-lookup"><span data-stu-id="b2505-123">The URL of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="b2505-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="b2505-124">-Location</span></span>
<span data-ttu-id="b2505-125">Azt a régiót adja meg, ahol ez a parancsmag hozza létre a fiókot.</span><span class="sxs-lookup"><span data-stu-id="b2505-125">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="b2505-126">További tudnivalókat az [Azure Regions](https://azure.microsoft.com/en-us/regions)című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="b2505-126">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="b2505-127">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="b2505-127">-PoolAllocationMode</span></span>
<span data-ttu-id="b2505-128">Gyűjtői mód a kötegek létrehozásához a köteg fiókban.</span><span class="sxs-lookup"><span data-stu-id="b2505-128">The allocation mode for creating pools in the Batch account.</span></span>

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

### <span data-ttu-id="b2505-129">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="b2505-129">-PublicNetworkAccess</span></span>
<span data-ttu-id="b2505-130">A nyilvános hálózati hozzáférés típusa</span><span class="sxs-lookup"><span data-stu-id="b2505-130">The public network access type</span></span>

```yaml
Type: Microsoft.Azure.Management.Batch.Models.PublicNetworkAccessType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2505-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2505-131">-ResourceGroupName</span></span>
<span data-ttu-id="b2505-132">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag létrehozza a fiókot.</span><span class="sxs-lookup"><span data-stu-id="b2505-132">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="b2505-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="b2505-133">-Tag</span></span>
<span data-ttu-id="b2505-134">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="b2505-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b2505-135">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="b2505-135">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b2505-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2505-136">CommonParameters</span></span>
<span data-ttu-id="b2505-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2505-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2505-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b2505-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2505-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2505-139">INPUTS</span></span>

### <span data-ttu-id="b2505-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b2505-140">System.String</span></span>

### <span data-ttu-id="b2505-141">System. null ' 1 [[Microsoft.Azure.Management.BatCH. Modellek. PoolAllocationMode, Microsoft.Azure.Management.BatCH, version = 9.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b2505-141">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=9.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b2505-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b2505-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b2505-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2505-143">OUTPUTS</span></span>

### <span data-ttu-id="b2505-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b2505-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b2505-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2505-145">NOTES</span></span>

## <span data-ttu-id="b2505-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2505-146">RELATED LINKS</span></span>

[<span data-ttu-id="b2505-147">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b2505-147">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="b2505-148">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b2505-148">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="b2505-149">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b2505-149">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="b2505-150">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b2505-150">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
