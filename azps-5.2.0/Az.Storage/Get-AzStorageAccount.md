---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ae7a43da35ce0aa41a34639521bc610d69843062
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349721"
---
# <span data-ttu-id="81856-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="81856-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="81856-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81856-102">SYNOPSIS</span></span>
<span data-ttu-id="81856-103">Tárfiókot kap.</span><span class="sxs-lookup"><span data-stu-id="81856-103">Gets a Storage account.</span></span>

## <span data-ttu-id="81856-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="81856-104">SYNTAX</span></span>

### <span data-ttu-id="81856-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="81856-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81856-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="81856-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81856-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="81856-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81856-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="81856-108">DESCRIPTION</span></span>
<span data-ttu-id="81856-109">A **Get-AzStorageAccount** parancsmag egy megadott tárfiókot vagy egy erőforráscsoport vagy az előfizetés összes tárfiókját megkapja.</span><span class="sxs-lookup"><span data-stu-id="81856-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="81856-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="81856-110">EXAMPLES</span></span>

### <span data-ttu-id="81856-111">1. példa: Adott tárfiók lekérte</span><span class="sxs-lookup"><span data-stu-id="81856-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="81856-112">Ez a parancs a megadott Tárfiókot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="81856-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="81856-113">2. példa: Erőforráscsoport összes tárfiókja</span><span class="sxs-lookup"><span data-stu-id="81856-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="81856-114">Ez a parancs egy erőforráscsoport összes tárfiókját beveszi.</span><span class="sxs-lookup"><span data-stu-id="81856-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="81856-115">3. példa: Az előfizetés összes tárfiókja lekérte</span><span class="sxs-lookup"><span data-stu-id="81856-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="81856-116">Ez a parancs az előfizetés összes tárfiókját beveszi.</span><span class="sxs-lookup"><span data-stu-id="81856-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="81856-117">4. példa: Tárfiókok lekérte blob-visszaállítási állapotát</span><span class="sxs-lookup"><span data-stu-id="81856-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="81856-118">Ez a parancs blob-visszaállítási állapottal rendelkező tárfiókokat kap, és a blob-visszaállítás állapotát mutatja.</span><span class="sxs-lookup"><span data-stu-id="81856-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="81856-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81856-119">PARAMETERS</span></span>

### <span data-ttu-id="81856-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81856-120">-AsJob</span></span>
<span data-ttu-id="81856-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="81856-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81856-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81856-122">-DefaultProfile</span></span>
<span data-ttu-id="81856-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81856-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81856-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="81856-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="81856-125">Szerezze be a BlobRestoreStatus tárfiókját.</span><span class="sxs-lookup"><span data-stu-id="81856-125">Get the BlobRestoreStatus of the Storage account.</span></span>

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

### <span data-ttu-id="81856-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="81856-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="81856-127">Szerezze be a Tárfiók GeoReplicationStats-ját.</span><span class="sxs-lookup"><span data-stu-id="81856-127">Get the GeoReplicationStats of the Storage account.</span></span>

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

### <span data-ttu-id="81856-128">-Name</span><span class="sxs-lookup"><span data-stu-id="81856-128">-Name</span></span>
<span data-ttu-id="81856-129">A lekért tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81856-129">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="81856-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81856-130">-ResourceGroupName</span></span>
<span data-ttu-id="81856-131">Annak az erőforráscsoportnak a neve, amely a behozni kívánt tárfiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="81856-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="81856-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81856-132">CommonParameters</span></span>
<span data-ttu-id="81856-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81856-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81856-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81856-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81856-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81856-135">INPUTS</span></span>

### <span data-ttu-id="81856-136">System.String</span><span class="sxs-lookup"><span data-stu-id="81856-136">System.String</span></span>

## <span data-ttu-id="81856-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81856-137">OUTPUTS</span></span>

### <span data-ttu-id="81856-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="81856-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="81856-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="81856-139">NOTES</span></span>

## <span data-ttu-id="81856-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81856-140">RELATED LINKS</span></span>

[<span data-ttu-id="81856-141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="81856-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="81856-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="81856-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="81856-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="81856-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


