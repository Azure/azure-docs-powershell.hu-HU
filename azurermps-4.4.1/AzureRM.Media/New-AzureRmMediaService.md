---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
ms.openlocfilehash: 86f1667c1383f226d47afed2a842af6386dad81e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679410"
---
# <span data-ttu-id="8b20b-101">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="8b20b-101">New-AzureRmMediaService</span></span>

## <span data-ttu-id="8b20b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b20b-102">SYNOPSIS</span></span>
<span data-ttu-id="8b20b-103">Médiafájlt hoz létre, ha már létezik a médiafájl, az összes tulajdonságát frissíti a program a megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="8b20b-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b20b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b20b-104">SYNTAX</span></span>

### <span data-ttu-id="8b20b-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="8b20b-105">StorageAccountIdParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b20b-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="8b20b-106">StorageAccountsParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b20b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b20b-107">DESCRIPTION</span></span>
<span data-ttu-id="8b20b-108">A **New-AzureRmMediaService** parancsmag létrehoz egy multimédiás szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="8b20b-108">The **New-AzureRmMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="8b20b-109">Ha már létezik a médiaszolgáltató, ez a parancsmag frissíti a tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="8b20b-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="8b20b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8b20b-110">EXAMPLES</span></span>

### <span data-ttu-id="8b20b-111">Example1: médiafájlok létrehozása csak az elsődleges tárterület-fiókkal</span><span class="sxs-lookup"><span data-stu-id="8b20b-111">Example1: Create a media service with the primary storage account only</span></span>
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
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tags $Tags
```

<span data-ttu-id="8b20b-112">Ebből a példaból megtudhatja, hogy miként hozhat létre médiafájlokat csak az elsődleges tárterület-fiók megadásával.</span><span class="sxs-lookup"><span data-stu-id="8b20b-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="8b20b-113">Ez a parancsfájl számos más parancsmagot használ.</span><span class="sxs-lookup"><span data-stu-id="8b20b-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="8b20b-114">2. példa: multimédiás szolgáltatás létrehozása több tárterülettel</span><span class="sxs-lookup"><span data-stu-id="8b20b-114">Example 2: Create a media service with multiple storage</span></span>
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
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tags $Tags
```

<span data-ttu-id="8b20b-115">Ez a példa bemutatja, hogyan hozhat létre multimédiás szolgáltatásokat több tárolási fiókkal.</span><span class="sxs-lookup"><span data-stu-id="8b20b-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="8b20b-116">Ez a parancsfájl számos más parancsmagot használ.</span><span class="sxs-lookup"><span data-stu-id="8b20b-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="8b20b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b20b-117">PARAMETERS</span></span>

### <span data-ttu-id="8b20b-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8b20b-118">-AccountName</span></span>
<span data-ttu-id="8b20b-119">Annak a médiafájlnak a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8b20b-119">Specifies the name of the media service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8b20b-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="8b20b-120">-Location</span></span>
<span data-ttu-id="8b20b-121">Azt a régiót adja meg, amelyre ez a parancsmag létrehozta a médiafájlt.</span><span class="sxs-lookup"><span data-stu-id="8b20b-121">Specifies the region that this cmdlet creates the media service in.</span></span>

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

### <span data-ttu-id="8b20b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b20b-122">-ResourceGroupName</span></span>
<span data-ttu-id="8b20b-123">Annak az erőforráscsoport-csoportnak a neve, amelyhez a médiafájl van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8b20b-123">Specifies the name of the resource group that the media service is assigned to.</span></span>

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

### <span data-ttu-id="8b20b-124">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8b20b-124">-StorageAccountId</span></span>
<span data-ttu-id="8b20b-125">A Media Service-fiókhoz társított tárterületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b20b-125">Specifies the storage account associated with the media service account.</span></span>

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

### <span data-ttu-id="8b20b-126">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="8b20b-126">-StorageAccounts</span></span>
<span data-ttu-id="8b20b-127">A Media szolgáltatáshoz társítani kívánt tárolási fiókok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b20b-127">Specifies an array of storage accounts to associate with the media service.</span></span>

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

### <span data-ttu-id="8b20b-128">-Címkék</span><span class="sxs-lookup"><span data-stu-id="8b20b-128">-Tags</span></span>
<span data-ttu-id="8b20b-129">A médiaszolgáltató címkéit adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b20b-129">Specifies tags for the media service.</span></span>

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

### <span data-ttu-id="8b20b-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8b20b-130">-Confirm</span></span>
<span data-ttu-id="8b20b-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8b20b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b20b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b20b-132">-WhatIf</span></span>
<span data-ttu-id="8b20b-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8b20b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b20b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8b20b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b20b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b20b-135">-DefaultProfile</span></span>
<span data-ttu-id="8b20b-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b20b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b20b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b20b-137">CommonParameters</span></span>
<span data-ttu-id="8b20b-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b20b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b20b-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b20b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b20b-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b20b-140">INPUTS</span></span>

## <span data-ttu-id="8b20b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b20b-141">OUTPUTS</span></span>

### <span data-ttu-id="8b20b-142">Microsoft. Azure. commands. Media. models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="8b20b-142">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="8b20b-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b20b-143">NOTES</span></span>

## <span data-ttu-id="8b20b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b20b-144">RELATED LINKS</span></span>

[<span data-ttu-id="8b20b-145">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="8b20b-145">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="8b20b-146">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="8b20b-146">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="8b20b-147">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="8b20b-147">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


