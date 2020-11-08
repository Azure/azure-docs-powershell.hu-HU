---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ae7a43da35ce0aa41a34639521bc610d69843062
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195473"
---
# <span data-ttu-id="4c641-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c641-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="4c641-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c641-102">SYNOPSIS</span></span>
<span data-ttu-id="4c641-103">Megkapja a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="4c641-103">Gets a Storage account.</span></span>

## <span data-ttu-id="4c641-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c641-104">SYNTAX</span></span>

### <span data-ttu-id="4c641-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c641-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c641-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c641-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c641-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c641-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c641-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c641-108">DESCRIPTION</span></span>
<span data-ttu-id="4c641-109">A **Get-AzStorageAccount** parancsmag egy erőforrás-csoportban vagy az előfizetésben megadott tárolási fiókot vagy minden tárolási fiókot kap.</span><span class="sxs-lookup"><span data-stu-id="4c641-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="4c641-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4c641-110">EXAMPLES</span></span>

### <span data-ttu-id="4c641-111">1. példa: megadott tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="4c641-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="4c641-112">Ez a parancs a megadott tárterület-fiókot kapja.</span><span class="sxs-lookup"><span data-stu-id="4c641-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="4c641-113">2. példa: az erőforráscsoport minden tárolási fiókjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="4c641-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="4c641-114">Ez a parancs egy erőforráscsoport minden tárolási fiókját beilleszti.</span><span class="sxs-lookup"><span data-stu-id="4c641-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="4c641-115">3. példa: az előfizetésben lévő összes tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="4c641-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="4c641-116">Ez a parancs az előfizetésben szereplő összes tárolási fiókot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="4c641-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="4c641-117">Példa 4: tárterület-fiókok beszerzése blob-visszaállítási állapottal</span><span class="sxs-lookup"><span data-stu-id="4c641-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="4c641-118">Ez a parancs tárolási fiókokat kap a blob-visszaállítási állapottal, és megjeleníti a blob-visszaállítás állapotát.</span><span class="sxs-lookup"><span data-stu-id="4c641-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="4c641-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c641-119">PARAMETERS</span></span>

### <span data-ttu-id="4c641-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c641-120">-AsJob</span></span>
<span data-ttu-id="4c641-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4c641-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c641-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c641-122">-DefaultProfile</span></span>
<span data-ttu-id="4c641-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c641-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c641-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="4c641-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="4c641-125">A BlobRestoreStatus beszerzése</span><span class="sxs-lookup"><span data-stu-id="4c641-125">Get the BlobRestoreStatus of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c641-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="4c641-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="4c641-127">A GeoReplicationStats beszerzése</span><span class="sxs-lookup"><span data-stu-id="4c641-127">Get the GeoReplicationStats of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c641-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c641-128">-Name</span></span>
<span data-ttu-id="4c641-129">A beszerzéshez használandó tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c641-129">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c641-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c641-130">-ResourceGroupName</span></span>
<span data-ttu-id="4c641-131">Annak a csoportnak a neve, amely a beszerzéshez használt tárolási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4c641-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c641-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c641-132">CommonParameters</span></span>
<span data-ttu-id="4c641-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c641-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c641-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c641-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c641-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c641-135">INPUTS</span></span>

### <span data-ttu-id="4c641-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4c641-136">System.String</span></span>

## <span data-ttu-id="4c641-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c641-137">OUTPUTS</span></span>

### <span data-ttu-id="4c641-138">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c641-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="4c641-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c641-139">NOTES</span></span>

## <span data-ttu-id="4c641-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c641-140">RELATED LINKS</span></span>

[<span data-ttu-id="4c641-141">Új – AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c641-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="4c641-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c641-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="4c641-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c641-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


