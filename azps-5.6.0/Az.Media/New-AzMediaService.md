---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/powershell/module/az.media/new-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
ms.openlocfilehash: 9ad314046ec9a1f1769042a2e36c64ddb0af0666
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006614"
---
# <span data-ttu-id="b65ea-101">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b65ea-101">New-AzMediaService</span></span>

## <span data-ttu-id="b65ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b65ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b65ea-103">Médiaszolgáltatást hoz létre, ha a médiaszolgáltatás már létezik, minden tulajdonsága frissül a megadott bemenettel.</span><span class="sxs-lookup"><span data-stu-id="b65ea-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

## <span data-ttu-id="b65ea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b65ea-104">SYNTAX</span></span>

### <span data-ttu-id="b65ea-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="b65ea-105">StorageAccountIdParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b65ea-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="b65ea-106">StorageAccountsParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b65ea-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b65ea-107">DESCRIPTION</span></span>
<span data-ttu-id="b65ea-108">A **New-AzMediaService** parancsmag médiaszolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b65ea-108">The **New-AzMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="b65ea-109">Ha a médiaszolgáltatás már létezik, ez a parancsmag frissíti a tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b65ea-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="b65ea-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b65ea-110">EXAMPLES</span></span>

### <span data-ttu-id="b65ea-111">Példa1: Médiaszolgáltatás létrehozása csak az elsődleges tárfiókkal</span><span class="sxs-lookup"><span data-stu-id="b65ea-111">Example1: Create a media service with the primary storage account only</span></span>
```
PS C:\># Variables
## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName = "Storage1"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tag $Tags
```

<span data-ttu-id="b65ea-112">Ez a példa azt mutatja be, hogy miként hozhat létre médiaszolgáltatást kizárólag elsődleges tárfiók megadásával.</span><span class="sxs-lookup"><span data-stu-id="b65ea-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="b65ea-113">Ez a parancsprogram számos más parancsmagot használ.</span><span class="sxs-lookup"><span data-stu-id="b65ea-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="b65ea-114">2. példa: Több tárterületet tároló médiaszolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="b65ea-114">Example 2: Create a media service with multiple storage</span></span>
```
PS C:\># Variables

## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName1 = "storage1"
$StorageName2 = "storage2"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tag $Tags
```

<span data-ttu-id="b65ea-115">Az alábbi példa bemutatja, hogy miként hozhat létre médiaszolgáltatást több tárfiókkal.</span><span class="sxs-lookup"><span data-stu-id="b65ea-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="b65ea-116">Ez a parancsprogram számos más parancsmagot használ.</span><span class="sxs-lookup"><span data-stu-id="b65ea-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="b65ea-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b65ea-117">PARAMETERS</span></span>

### <span data-ttu-id="b65ea-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b65ea-118">-AccountName</span></span>
<span data-ttu-id="b65ea-119">A parancsmag által létrehozott médiaszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="b65ea-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65ea-120">-DefaultProfile</span></span>
<span data-ttu-id="b65ea-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b65ea-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b65ea-122">-Location</span><span class="sxs-lookup"><span data-stu-id="b65ea-122">-Location</span></span>
<span data-ttu-id="b65ea-123">Azt a régiót adja meg, ahol a parancsmag létrehozza a médiaszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b65ea-123">Specifies the region that this cmdlet creates the media service in.</span></span>

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

### <span data-ttu-id="b65ea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b65ea-124">-ResourceGroupName</span></span>
<span data-ttu-id="b65ea-125">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a médiaszolgáltatás hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b65ea-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65ea-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b65ea-126">-StorageAccountId</span></span>
<span data-ttu-id="b65ea-127">A médiaszolgáltatás-fiókhoz társított tárfiók.</span><span class="sxs-lookup"><span data-stu-id="b65ea-127">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65ea-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="b65ea-128">-StorageAccounts</span></span>
<span data-ttu-id="b65ea-129">A médiaszolgáltatáshoz társítandó tárfiókok tömbje.</span><span class="sxs-lookup"><span data-stu-id="b65ea-129">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65ea-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="b65ea-130">-Tag</span></span>
<span data-ttu-id="b65ea-131">A médiaszolgáltatás-fiókhoz társított címkék.</span><span class="sxs-lookup"><span data-stu-id="b65ea-131">The tags associated with the media service account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b65ea-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b65ea-132">-Confirm</span></span>
<span data-ttu-id="b65ea-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b65ea-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b65ea-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b65ea-134">-WhatIf</span></span>
<span data-ttu-id="b65ea-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b65ea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b65ea-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b65ea-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b65ea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65ea-137">CommonParameters</span></span>
<span data-ttu-id="b65ea-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b65ea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65ea-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b65ea-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65ea-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b65ea-140">INPUTS</span></span>

### <span data-ttu-id="b65ea-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b65ea-141">System.String</span></span>

### <span data-ttu-id="b65ea-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="b65ea-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="b65ea-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b65ea-143">OUTPUTS</span></span>

### <span data-ttu-id="b65ea-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="b65ea-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="b65ea-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b65ea-145">NOTES</span></span>

## <span data-ttu-id="b65ea-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b65ea-146">RELATED LINKS</span></span>

[<span data-ttu-id="b65ea-147">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b65ea-147">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="b65ea-148">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b65ea-148">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="b65ea-149">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b65ea-149">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


